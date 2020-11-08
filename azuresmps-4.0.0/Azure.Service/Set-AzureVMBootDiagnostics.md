---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 846B9EB8-8EC2-4BDA-90EF-59098696F460
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c4e1dedb02286ceaab182e0912198c23ec03ee5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054759"
---
# <span data-ttu-id="6c361-101">Set-AzureVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="6c361-101">Set-AzureVMBootDiagnostics</span></span>

## <span data-ttu-id="6c361-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c361-102">SYNOPSIS</span></span>

## <span data-ttu-id="6c361-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c361-103">SYNTAX</span></span>

### <span data-ttu-id="6c361-104">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="6c361-104">EnableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Enable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6c361-105">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="6c361-105">DisableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6c361-106">Opis</span><span class="sxs-lookup"><span data-stu-id="6c361-106">DESCRIPTION</span></span>

## <span data-ttu-id="6c361-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c361-107">EXAMPLES</span></span>

### <span data-ttu-id="6c361-108">1:1</span><span class="sxs-lookup"><span data-stu-id="6c361-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="6c361-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c361-109">PARAMETERS</span></span>

### <span data-ttu-id="6c361-110">-Disable</span><span class="sxs-lookup"><span data-stu-id="6c361-110">-Disable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c361-111">-Enable</span><span class="sxs-lookup"><span data-stu-id="6c361-111">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c361-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6c361-112">-InformationAction</span></span>
<span data-ttu-id="6c361-113">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="6c361-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6c361-114">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6c361-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6c361-115">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="6c361-115">Continue</span></span>
- <span data-ttu-id="6c361-116">Ignorować</span><span class="sxs-lookup"><span data-stu-id="6c361-116">Ignore</span></span>
- <span data-ttu-id="6c361-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="6c361-117">Inquire</span></span>
- <span data-ttu-id="6c361-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6c361-118">SilentlyContinue</span></span>
- <span data-ttu-id="6c361-119">Przestaw</span><span class="sxs-lookup"><span data-stu-id="6c361-119">Stop</span></span>
- <span data-ttu-id="6c361-120">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="6c361-120">Suspend</span></span>

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

### <span data-ttu-id="6c361-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6c361-121">-InformationVariable</span></span>
<span data-ttu-id="6c361-122">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="6c361-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6c361-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="6c361-123">-Profile</span></span>
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

### <span data-ttu-id="6c361-124">-VM</span><span class="sxs-lookup"><span data-stu-id="6c361-124">-VM</span></span>
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

### <span data-ttu-id="6c361-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c361-125">CommonParameters</span></span>
<span data-ttu-id="6c361-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c361-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c361-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c361-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c361-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c361-128">INPUTS</span></span>

## <span data-ttu-id="6c361-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c361-129">OUTPUTS</span></span>

## <span data-ttu-id="6c361-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c361-130">NOTES</span></span>

## <span data-ttu-id="6c361-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c361-131">RELATED LINKS</span></span>

