---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: EB68FC6B-310F-41DB-B870-B907147F8513
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: e61136122873f7837120065194252aba145ea733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552331"
---
# <span data-ttu-id="da93b-101">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="da93b-101">Get-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="da93b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da93b-102">SYNOPSIS</span></span>
<span data-ttu-id="da93b-103">Pobiera informacje dotyczące dostawców usługi Azure Site Recovery w magazynie.</span><span class="sxs-lookup"><span data-stu-id="da93b-103">Gets information on the Azure Site Recovery providers in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da93b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da93b-104">SYNTAX</span></span>

### <span data-ttu-id="da93b-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="da93b-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da93b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="da93b-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da93b-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="da93b-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da93b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="da93b-108">DESCRIPTION</span></span>
<span data-ttu-id="da93b-109">Polecenie cmdlet **Get-AzureRmSiteRecoveryServicesProvider** pobiera informacje dotyczące dostawców usługi Azure Site Recovery w magazynie.</span><span class="sxs-lookup"><span data-stu-id="da93b-109">The **Get-AzureRmSiteRecoveryServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="da93b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da93b-110">EXAMPLES</span></span>

## <span data-ttu-id="da93b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da93b-111">PARAMETERS</span></span>

### <span data-ttu-id="da93b-112">-Fabric</span><span class="sxs-lookup"><span data-stu-id="da93b-112">-Fabric</span></span>
<span data-ttu-id="da93b-113">Określa obiekt sieci szkieletowej usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="da93b-113">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da93b-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="da93b-114">-FriendlyName</span></span>
<span data-ttu-id="da93b-115">Określa przyjazną nazwę dostawcy usługi Azure Site Recovery, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da93b-115">Specifies the friendly name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

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

### <span data-ttu-id="da93b-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="da93b-116">-Name</span></span>
<span data-ttu-id="da93b-117">Określa nazwę dostawcy usługi Azure Site Recovery, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da93b-117">Specifies the name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

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

### <span data-ttu-id="da93b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da93b-118">-DefaultProfile</span></span>
<span data-ttu-id="da93b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da93b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da93b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da93b-120">CommonParameters</span></span>
<span data-ttu-id="da93b-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da93b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da93b-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da93b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da93b-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da93b-123">INPUTS</span></span>

### <span data-ttu-id="da93b-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="da93b-124">ASRFabric</span></span>
<span data-ttu-id="da93b-125">Parametr "Fabric" akceptuje wartość typu "ASRFabric" z procesu</span><span class="sxs-lookup"><span data-stu-id="da93b-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="da93b-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da93b-126">OUTPUTS</span></span>

### <span data-ttu-id="da93b-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="da93b-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="da93b-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da93b-128">NOTES</span></span>

## <span data-ttu-id="da93b-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da93b-129">RELATED LINKS</span></span>

[<span data-ttu-id="da93b-130">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="da93b-130">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="da93b-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="da93b-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
