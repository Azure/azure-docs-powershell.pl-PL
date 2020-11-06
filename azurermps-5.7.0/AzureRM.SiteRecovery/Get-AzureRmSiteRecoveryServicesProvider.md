---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: EB68FC6B-310F-41DB-B870-B907147F8513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 4e65636c732ede20487df0b80973172977c6c832
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551555"
---
# <span data-ttu-id="d1c1f-101">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="d1c1f-101">Get-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="d1c1f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d1c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c1f-103">Pobiera informacje dotyczące dostawców usługi Azure Site Recovery w magazynie.</span><span class="sxs-lookup"><span data-stu-id="d1c1f-103">Gets information on the Azure Site Recovery providers in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1c1f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d1c1f-104">SYNTAX</span></span>

### <span data-ttu-id="d1c1f-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d1c1f-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1c1f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d1c1f-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1c1f-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d1c1f-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1c1f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d1c1f-108">DESCRIPTION</span></span>
<span data-ttu-id="d1c1f-109">Polecenie cmdlet **Get-AzureRmSiteRecoveryServicesProvider** pobiera informacje dotyczące dostawców usługi Azure Site Recovery w magazynie.</span><span class="sxs-lookup"><span data-stu-id="d1c1f-109">The **Get-AzureRmSiteRecoveryServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="d1c1f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d1c1f-110">EXAMPLES</span></span>

## <span data-ttu-id="d1c1f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1c1f-111">PARAMETERS</span></span>

### <span data-ttu-id="d1c1f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c1f-112">-DefaultProfile</span></span>
<span data-ttu-id="d1c1f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1c1f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1c1f-114">-Fabric</span><span class="sxs-lookup"><span data-stu-id="d1c1f-114">-Fabric</span></span>
<span data-ttu-id="d1c1f-115">Określa obiekt sieci szkieletowej usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d1c1f-115">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1c1f-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d1c1f-116">-FriendlyName</span></span>
<span data-ttu-id="d1c1f-117">Określa przyjazną nazwę dostawcy usługi Azure Site Recovery, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1c1f-117">Specifies the friendly name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d1c1f-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d1c1f-118">-Name</span></span>
<span data-ttu-id="d1c1f-119">Określa nazwę dostawcy usługi Azure Site Recovery, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1c1f-119">Specifies the name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d1c1f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c1f-120">CommonParameters</span></span>
<span data-ttu-id="d1c1f-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1c1f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c1f-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1c1f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c1f-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1c1f-123">INPUTS</span></span>

### <span data-ttu-id="d1c1f-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d1c1f-124">ASRFabric</span></span>
<span data-ttu-id="d1c1f-125">Parametr "Fabric" akceptuje wartość typu "ASRFabric" z procesu</span><span class="sxs-lookup"><span data-stu-id="d1c1f-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="d1c1f-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d1c1f-126">OUTPUTS</span></span>

### <span data-ttu-id="d1c1f-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d1c1f-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d1c1f-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d1c1f-128">NOTES</span></span>

## <span data-ttu-id="d1c1f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1c1f-129">RELATED LINKS</span></span>

[<span data-ttu-id="d1c1f-130">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="d1c1f-130">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="d1c1f-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="d1c1f-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
