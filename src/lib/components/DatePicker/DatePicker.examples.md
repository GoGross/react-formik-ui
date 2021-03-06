See [ReactJS Datepicker documentation](https://github.com/Hacker0x01/react-datepicker/blob/master/docs/datepicker.md) for a list of additional props and configurations

##### Default

```jsx
import { Formik } from 'formik'
import { Form, Datepicker, SubmitBtn } from 'react-formik-ui';

<Formik
  initialValues={{
    dateExample1: ''
  }}
  onSubmit={data => (alert(JSON.stringify(data)))}
>
  <Form>

    <Datepicker
      name='dateExample1'
      label='Select a date'
    />

    <SubmitBtn />
  </Form>
</Formik>
```

##### Structured

```jsx
import { Formik } from 'formik'
import { Form, Datepicker, SubmitBtn } from 'react-formik-ui';

<Formik
  initialValues={{
    dateExample2: ''
  }}
  onSubmit={data => (alert(JSON.stringify(data)))}
>
  <Form mode='structured'>

    <Datepicker
      name='dateExample2'
      label='Select a date'
    />

    <SubmitBtn />
  </Form>
</Formik>
```

##### Structured Required

```jsx
import { Formik } from 'formik'
import * as yup from 'yup'
import { Form, Datepicker, SubmitBtn } from 'react-formik-ui';

const getSchema = () => {
  return yup.object().shape({
    dateExampleRequired: yup
      .date()
      .required('Is required'),
  });
};

<Formik
  initialValues={{
    dateExampleRequired: ''
  }}
  validationSchema={getSchema}
  onSubmit={data => (alert(JSON.stringify(data)))}
>
  <Form mode='structured'>

    <Datepicker
      name='dateExampleRequired'
      label='Select a date'
      dateFormat='dd.MM.yyyy'
      placeholder='dd.mm.yyyy'
      hint='Please enter / select a date'
      required
    />

    <SubmitBtn />
  </Form>
</Formik>
```


##### with Keyboard Navigation enabled

```jsx
import { Formik } from 'formik'
import { Form, Datepicker, SubmitBtn } from 'react-formik-ui';

<Formik
  initialValues={{
    dateExample8: ''
  }}
  onSubmit={data => (alert(JSON.stringify(data)))}
>
  <Form mode='structured'>

    <Datepicker
      name='dateExample8'
      label='Select a date'
      disabledKeyboardNavigation={false}
    />

    <SubmitBtn />
  </Form>
</Formik>
```

##### Themed

```jsx
import { Formik } from 'formik'
import { Form, Datepicker, SubmitBtn } from 'react-formik-ui';

<Formik
  initialValues={{
    dateExample3: ''
  }}
  onSubmit={data => (alert(JSON.stringify(data)))}
>
  <Form mode='themed'>
    <Datepicker
      name='dateExample3'
      label='Select a date'
      hint='DD.MM.YYYY'
    />

    <SubmitBtn />
  </Form>
</Formik>
```

##### Themed with placeholder

```jsx
import { Formik } from 'formik'
import { Form, Datepicker, SubmitBtn } from 'react-formik-ui';

<Formik
  initialValues={{
    dateExample4: ''
  }}
  onSubmit={data => (alert(JSON.stringify(data)))}
>
  <Form mode='themed'>

    <Datepicker
      name='dateExample4'
      label='Select a date'
      placeholder='DD.MM.YYYYY'
      dateFormat='dd.MM.yyyy'
    />

    <SubmitBtn />
  </Form>
</Formik>
```

##### Themed with time picker

```jsx
import { Formik } from 'formik'
import { Form, Datepicker, SubmitBtn } from 'react-formik-ui';

<Formik
  initialValues={{
    dateExample5: ''
  }}
  onSubmit={data => (alert(JSON.stringify(data)))}
>
  <Form mode='themed'>

    <Datepicker
      name='dateExample5'
      label='Select a date and time'
      showTimeSelect
      timeFormat="HH:mm"
      timeIntervals={30}
      dateFormat="dd.MM.yyyy hh:mm aa"
      timeCaption="time"
      minDate={new Date()}
    />

    <SubmitBtn />
  </Form>
</Formik>
```

##### Themed and disabled

```jsx
import { Formik } from 'formik'
import { Form, Datepicker, SubmitBtn } from 'react-formik-ui';

<Formik
  initialValues={{
    dateExample6: ''
  }}
  onSubmit={data => (alert(JSON.stringify(data)))}
>
  <Form mode='themed'>

    <Datepicker
      name='dateExample6'
      label='Select a date'
      disabled
    />

    <SubmitBtn />
  </Form>
</Formik>
```

##### Themed disabled with placeholder

```jsx
import { Formik } from 'formik'
import { Form, Datepicker, SubmitBtn } from 'react-formik-ui';

<Formik
  initialValues={{
    dateExample7: ''
  }}
  onSubmit={data => (alert(JSON.stringify(data)))}
>
  <Form mode='themed'>

    <Datepicker
      name='dateExample7'
      label='Select a date'
      placeholder='DD.MM.YYYYY'
      dateFormat='dd.MM.yyyy'
      disabled
    />

    <SubmitBtn />
  </Form>
</Formik>
```
