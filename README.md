# mui-guide
Personal guide for MUI. 

# MUI 5
Two ways to style a component, use sx or styled component

# sx example usage
- It is a shorthand for custom style. 
- sx is integrated with theme in order words it is theme consicious. 
- Used mainly for component/compound specific styling. 

# sx example usage

```
<Box sx={{ p: 2 }} // p shorthand for padding and 2 is 2 * 4 (theme) so 8px
<Box sx={{ backgroundColor: 'primary.main' }} // theme primary main color
<Box sx={{ height: (theme) => theme.spacing(10) }} // theme is accessible
```

# sx conditional usage
```
const foo = true // somewhere in the code, no need for classNames
<Box
  sx={[
    {
      '&:hover': {
        color: 'red',
        backgroundColor: 'white',
      },
    },
    foo && {
      '&:hover': { backgroundColor: 'grey' },
    }
  ]}
/>

```

For more details, check out MUI documentation. Above is taken directly from MUI docs
