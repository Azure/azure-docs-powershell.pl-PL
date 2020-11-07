---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaddomainextension
schema: 2.0.0
ms.openlocfilehash: 01a5a69053cfd05186abae45d5b53fff0b022b98
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898054"
---
# <span data-ttu-id="9be52-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="9be52-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="9be52-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9be52-102">SYNOPSIS</span></span>
<span data-ttu-id="9be52-103">Pobiera informacje o rozszerzeniu domeny usługi AD.</span><span class="sxs-lookup"><span data-stu-id="9be52-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9be52-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9be52-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9be52-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9be52-105">DESCRIPTION</span></span>
<span data-ttu-id="9be52-106">Polecenie cmdlet **Get-AzureRmVMADDomainExtension** pobiera informacje o określonym rozszerzeniu domeny usługi Azure Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="9be52-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="9be52-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9be52-107">EXAMPLES</span></span>

### <span data-ttu-id="9be52-108">1:1</span><span class="sxs-lookup"><span data-stu-id="9be52-108">1:</span></span>
```

```

## <span data-ttu-id="9be52-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9be52-109">PARAMETERS</span></span>

### <span data-ttu-id="9be52-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9be52-110">-DefaultProfile</span></span>
<span data-ttu-id="9be52-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9be52-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be52-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9be52-112">-Name</span></span>
<span data-ttu-id="9be52-113">Określa nazwę rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="9be52-113">Specifies the name of the domain extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9be52-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9be52-114">-ResourceGroupName</span></span>
<span data-ttu-id="9be52-115">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9be52-115">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9be52-116">-Status</span><span class="sxs-lookup"><span data-stu-id="9be52-116">-Status</span></span>
<span data-ttu-id="9be52-117">Wskazuje, że to polecenie cmdlet pobiera widok wystąpienia rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="9be52-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9be52-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="9be52-118">-VMName</span></span>
<span data-ttu-id="9be52-119">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9be52-119">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9be52-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9be52-120">CommonParameters</span></span>
<span data-ttu-id="9be52-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9be52-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9be52-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9be52-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9be52-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9be52-123">INPUTS</span></span>

### <span data-ttu-id="9be52-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9be52-124">None</span></span>
<span data-ttu-id="9be52-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9be52-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9be52-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9be52-126">OUTPUTS</span></span>

### <span data-ttu-id="9be52-127">Microsoft. Azure. Commands. COMPUTE. models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="9be52-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="9be52-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9be52-128">NOTES</span></span>

## <span data-ttu-id="9be52-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9be52-129">RELATED LINKS</span></span>

[<span data-ttu-id="9be52-130">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="9be52-130">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


