---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 28EEB54B-C8C9-4C20-9454-5069C23583B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 591cbcbc4663bde7b9d6e9bd4e35a1e91728cd85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542919"
---
# <span data-ttu-id="6f2bd-101">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="6f2bd-101">Get-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="6f2bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6f2bd-102">SYNOPSIS</span></span>
<span data-ttu-id="6f2bd-103">Pobierz właściwości sieci szkieletowej odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="6f2bd-103">Get the properties of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f2bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6f2bd-104">SYNTAX</span></span>

### <span data-ttu-id="6f2bd-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="6f2bd-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f2bd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6f2bd-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f2bd-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6f2bd-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f2bd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6f2bd-108">DESCRIPTION</span></span>
<span data-ttu-id="6f2bd-109">Polecenie cmdlet **Get-AzureRmSiteRecoveryFabric** pobiera właściwości określonej sieci szkieletowej odzyskiwania witryny platformy Azure lub całej sieci szkieletowej odzyskiwania witryny Azure w magazynie usługi odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6f2bd-109">The **Get-AzureRmSiteRecoveryFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="6f2bd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6f2bd-110">EXAMPLES</span></span>

## <span data-ttu-id="6f2bd-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6f2bd-111">PARAMETERS</span></span>

### <span data-ttu-id="6f2bd-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6f2bd-112">-FriendlyName</span></span>
<span data-ttu-id="6f2bd-113">Określa przyjazną nazwę sieci szkieletowej odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="6f2bd-113">Specifies the friendly name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2bd-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6f2bd-114">-Name</span></span>
<span data-ttu-id="6f2bd-115">Określa nazwę sieci szkieletowej odzyskiwania witryny usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="6f2bd-115">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f2bd-116">-DefaultProfile</span></span>
<span data-ttu-id="6f2bd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6f2bd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2bd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f2bd-118">CommonParameters</span></span>
<span data-ttu-id="6f2bd-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f2bd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f2bd-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f2bd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f2bd-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f2bd-121">INPUTS</span></span>

## <span data-ttu-id="6f2bd-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6f2bd-122">OUTPUTS</span></span>

### <span data-ttu-id="6f2bd-123">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6f2bd-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6f2bd-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6f2bd-124">NOTES</span></span>

## <span data-ttu-id="6f2bd-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f2bd-125">RELATED LINKS</span></span>

[<span data-ttu-id="6f2bd-126">Nowe — AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="6f2bd-126">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="6f2bd-127">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="6f2bd-127">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
