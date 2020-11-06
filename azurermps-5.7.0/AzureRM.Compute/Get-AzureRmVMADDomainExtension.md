---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: d55d84560ca75a508a05276d8d33eb78d1d50ab5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546880"
---
# <span data-ttu-id="b05ea-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b05ea-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="b05ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b05ea-102">SYNOPSIS</span></span>
<span data-ttu-id="b05ea-103">Pobiera informacje o rozszerzeniu domeny usługi AD.</span><span class="sxs-lookup"><span data-stu-id="b05ea-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b05ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b05ea-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="b05ea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b05ea-105">DESCRIPTION</span></span>
<span data-ttu-id="b05ea-106">Polecenie cmdlet **Get-AzureRmVMADDomainExtension** pobiera informacje o określonym rozszerzeniu domeny usługi Azure Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="b05ea-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="b05ea-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b05ea-107">EXAMPLES</span></span>

## <span data-ttu-id="b05ea-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b05ea-108">PARAMETERS</span></span>

### <span data-ttu-id="b05ea-109">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b05ea-109">-Name</span></span>
<span data-ttu-id="b05ea-110">Określa nazwę rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="b05ea-110">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="b05ea-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b05ea-111">-ResourceGroupName</span></span>
<span data-ttu-id="b05ea-112">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b05ea-112">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b05ea-113">-Status</span><span class="sxs-lookup"><span data-stu-id="b05ea-113">-Status</span></span>
<span data-ttu-id="b05ea-114">Wskazuje, że to polecenie cmdlet pobiera widok wystąpienia rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="b05ea-114">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="b05ea-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="b05ea-115">-VMName</span></span>
<span data-ttu-id="b05ea-116">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b05ea-116">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="b05ea-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b05ea-117">CommonParameters</span></span>
<span data-ttu-id="b05ea-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b05ea-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b05ea-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b05ea-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b05ea-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b05ea-120">INPUTS</span></span>

### <span data-ttu-id="b05ea-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b05ea-121">None</span></span>
<span data-ttu-id="b05ea-122">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b05ea-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b05ea-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b05ea-123">OUTPUTS</span></span>

## <span data-ttu-id="b05ea-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b05ea-124">NOTES</span></span>

## <span data-ttu-id="b05ea-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b05ea-125">RELATED LINKS</span></span>

[<span data-ttu-id="b05ea-126">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b05ea-126">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


