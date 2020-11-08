---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EC6F7790-5E31-4C22-B006-38B5C1868671
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0272740ced33d19e2610a6116812df4a815ea3c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055154"
---
# <span data-ttu-id="21260-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="21260-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="21260-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21260-102">SYNOPSIS</span></span>

## <span data-ttu-id="21260-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21260-103">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-Enable] [[-CredentialName] <String>]
 [[-AzureKeyVaultUrl] <String>] [[-ServicePrincipalName] <String>] [[-ServicePrincipalSecret] <SecureString>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="21260-104">Opis</span><span class="sxs-lookup"><span data-stu-id="21260-104">DESCRIPTION</span></span>

## <span data-ttu-id="21260-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21260-105">EXAMPLES</span></span>

### <span data-ttu-id="21260-106">1:1</span><span class="sxs-lookup"><span data-stu-id="21260-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="21260-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21260-107">PARAMETERS</span></span>

### <span data-ttu-id="21260-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="21260-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21260-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="21260-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21260-110">-Enable</span><span class="sxs-lookup"><span data-stu-id="21260-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21260-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="21260-111">-InformationAction</span></span>
<span data-ttu-id="21260-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="21260-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="21260-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="21260-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="21260-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="21260-114">Continue</span></span>
- <span data-ttu-id="21260-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="21260-115">Ignore</span></span>
- <span data-ttu-id="21260-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="21260-116">Inquire</span></span>
- <span data-ttu-id="21260-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="21260-117">SilentlyContinue</span></span>
- <span data-ttu-id="21260-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="21260-118">Stop</span></span>
- <span data-ttu-id="21260-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="21260-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21260-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="21260-120">-InformationVariable</span></span>
<span data-ttu-id="21260-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="21260-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21260-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="21260-122">-Profile</span></span>
```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21260-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="21260-123">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21260-124">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="21260-124">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21260-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21260-125">CommonParameters</span></span>
<span data-ttu-id="21260-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21260-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21260-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21260-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21260-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21260-128">INPUTS</span></span>

## <span data-ttu-id="21260-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21260-129">OUTPUTS</span></span>

## <span data-ttu-id="21260-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21260-130">NOTES</span></span>

## <span data-ttu-id="21260-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21260-131">RELATED LINKS</span></span>

