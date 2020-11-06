---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: dde3873c7fe7ee18ee4745af967eb222833029d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527346"
---
# <span data-ttu-id="caa83-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="caa83-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="caa83-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="caa83-102">SYNOPSIS</span></span>
<span data-ttu-id="caa83-103">Zapoznaj się z informacjami na temat sieci szkieletowej odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="caa83-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caa83-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="caa83-104">SYNTAX</span></span>

### <span data-ttu-id="caa83-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="caa83-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [<CommonParameters>]
```

### <span data-ttu-id="caa83-106">ByName</span><span class="sxs-lookup"><span data-stu-id="caa83-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="caa83-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="caa83-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="caa83-108">Opis</span><span class="sxs-lookup"><span data-stu-id="caa83-108">DESCRIPTION</span></span>
<span data-ttu-id="caa83-109">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrFabric** pobiera właściwości określonej sieci szkieletowej odzyskiwania witryny platformy Azure lub całej sieci szkieletowej odzyskiwania witryny Azure w magazynie usługi odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="caa83-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="caa83-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="caa83-110">EXAMPLES</span></span>

### <span data-ttu-id="caa83-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="caa83-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="caa83-112">Zwraca wszystkie materiały szkieletowe odzyskiwania witryny Azure w magazynie.</span><span class="sxs-lookup"><span data-stu-id="caa83-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

## <span data-ttu-id="caa83-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="caa83-113">PARAMETERS</span></span>

### <span data-ttu-id="caa83-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="caa83-114">-FriendlyName</span></span>
<span data-ttu-id="caa83-115">Wyszukiwanie w sieci szkieletowej ASR według przyjaznej nazwy sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="caa83-115">Search for the ASR fabric by the friendly name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa83-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="caa83-116">-Name</span></span>
<span data-ttu-id="caa83-117">Wyszukiwanie w sieci szkieletowej ASR według nazwy sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="caa83-117">Search for the ASR fabric by the name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa83-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caa83-118">CommonParameters</span></span>
<span data-ttu-id="caa83-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caa83-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caa83-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caa83-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caa83-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="caa83-121">INPUTS</span></span>

### <span data-ttu-id="caa83-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="caa83-122">None</span></span>

## <span data-ttu-id="caa83-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="caa83-123">OUTPUTS</span></span>

### <span data-ttu-id="caa83-124">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="caa83-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="caa83-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="caa83-125">NOTES</span></span>

## <span data-ttu-id="caa83-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="caa83-126">RELATED LINKS</span></span>

[<span data-ttu-id="caa83-127">Nowe — AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="caa83-127">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="caa83-128">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="caa83-128">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
