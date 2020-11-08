---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EE96AC92-02A8-4A40-A26D-0882673E51A5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2dca85290564217f5c4c319ef3531d4c31500fcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055550"
---
# <span data-ttu-id="66597-101">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="66597-101">Get-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="66597-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66597-102">SYNOPSIS</span></span>

## <span data-ttu-id="66597-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66597-103">SYNTAX</span></span>

```
Get-AzureNetworkInterfaceConfig [[-Name] <String>] -VM <PersistentVMRoleContext>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="66597-104">Opis</span><span class="sxs-lookup"><span data-stu-id="66597-104">DESCRIPTION</span></span>

## <span data-ttu-id="66597-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66597-105">EXAMPLES</span></span>

### <span data-ttu-id="66597-106">1:1</span><span class="sxs-lookup"><span data-stu-id="66597-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="66597-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66597-107">PARAMETERS</span></span>

### <span data-ttu-id="66597-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="66597-108">-InformationAction</span></span>
<span data-ttu-id="66597-109">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="66597-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="66597-110">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="66597-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="66597-111">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="66597-111">Continue</span></span>
- <span data-ttu-id="66597-112">Ignorować</span><span class="sxs-lookup"><span data-stu-id="66597-112">Ignore</span></span>
- <span data-ttu-id="66597-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="66597-113">Inquire</span></span>
- <span data-ttu-id="66597-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="66597-114">SilentlyContinue</span></span>
- <span data-ttu-id="66597-115">Przestaw</span><span class="sxs-lookup"><span data-stu-id="66597-115">Stop</span></span>
- <span data-ttu-id="66597-116">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="66597-116">Suspend</span></span>

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

### <span data-ttu-id="66597-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="66597-117">-InformationVariable</span></span>
<span data-ttu-id="66597-118">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="66597-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="66597-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="66597-119">-Name</span></span>
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

### <span data-ttu-id="66597-120">-VM</span><span class="sxs-lookup"><span data-stu-id="66597-120">-VM</span></span>
```yaml
Type: PersistentVMRoleContext
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66597-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66597-121">CommonParameters</span></span>
<span data-ttu-id="66597-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66597-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66597-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66597-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66597-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66597-124">INPUTS</span></span>

## <span data-ttu-id="66597-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66597-125">OUTPUTS</span></span>

## <span data-ttu-id="66597-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66597-126">NOTES</span></span>

## <span data-ttu-id="66597-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66597-127">RELATED LINKS</span></span>

[<span data-ttu-id="66597-128">Dodaj-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="66597-128">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="66597-129">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="66597-129">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="66597-130">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="66597-130">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


