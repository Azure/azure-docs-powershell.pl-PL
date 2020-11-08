---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6AB4700D-571B-497A-9742-2654844553B6
online version: ''
schema: 2.0.0
ms.openlocfilehash: b46f15053639ec295d958766dac846d4f95e0368
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055117"
---
# <span data-ttu-id="944e4-101">Remove-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="944e4-101">Remove-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="944e4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="944e4-102">SYNOPSIS</span></span>

## <span data-ttu-id="944e4-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="944e4-103">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroupConfig [[-NetworkSecurityGroupName] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="944e4-104">Opis</span><span class="sxs-lookup"><span data-stu-id="944e4-104">DESCRIPTION</span></span>

## <span data-ttu-id="944e4-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="944e4-105">EXAMPLES</span></span>

### <span data-ttu-id="944e4-106">1:1</span><span class="sxs-lookup"><span data-stu-id="944e4-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="944e4-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="944e4-107">PARAMETERS</span></span>

### <span data-ttu-id="944e4-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="944e4-108">-InformationAction</span></span>
<span data-ttu-id="944e4-109">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="944e4-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="944e4-110">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="944e4-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="944e4-111">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="944e4-111">Continue</span></span>
- <span data-ttu-id="944e4-112">Ignorować</span><span class="sxs-lookup"><span data-stu-id="944e4-112">Ignore</span></span>
- <span data-ttu-id="944e4-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="944e4-113">Inquire</span></span>
- <span data-ttu-id="944e4-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="944e4-114">SilentlyContinue</span></span>
- <span data-ttu-id="944e4-115">Przestaw</span><span class="sxs-lookup"><span data-stu-id="944e4-115">Stop</span></span>
- <span data-ttu-id="944e4-116">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="944e4-116">Suspend</span></span>

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

### <span data-ttu-id="944e4-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="944e4-117">-InformationVariable</span></span>
<span data-ttu-id="944e4-118">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="944e4-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="944e4-119">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="944e4-119">-NetworkSecurityGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="944e4-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="944e4-120">-Profile</span></span>
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

### <span data-ttu-id="944e4-121">-VM</span><span class="sxs-lookup"><span data-stu-id="944e4-121">-VM</span></span>
```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="944e4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="944e4-122">CommonParameters</span></span>
<span data-ttu-id="944e4-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="944e4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="944e4-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="944e4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="944e4-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="944e4-125">INPUTS</span></span>

## <span data-ttu-id="944e4-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="944e4-126">OUTPUTS</span></span>

## <span data-ttu-id="944e4-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="944e4-127">NOTES</span></span>

## <span data-ttu-id="944e4-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="944e4-128">RELATED LINKS</span></span>

[<span data-ttu-id="944e4-129">Set-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="944e4-129">Set-AzureNetworkSecurityGroupConfig</span></span>](./Set-AzureNetworkSecurityGroupConfig.md)


