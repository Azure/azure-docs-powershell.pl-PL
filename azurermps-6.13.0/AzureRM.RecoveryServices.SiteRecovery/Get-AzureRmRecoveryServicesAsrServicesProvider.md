---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 506009ac15fa1c9eeeb3e0b7ae902e3c42d1d468
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718598"
---
# <span data-ttu-id="54666-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="54666-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="54666-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="54666-102">SYNOPSIS</span></span>
<span data-ttu-id="54666-103">Umożliwia wyświetlenie szczegółów dotyczących dostawców usług odzyskiwania ASR zarejestrowanych w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="54666-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54666-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="54666-104">SYNTAX</span></span>

### <span data-ttu-id="54666-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="54666-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54666-106">ByName</span><span class="sxs-lookup"><span data-stu-id="54666-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54666-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="54666-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54666-108">Opis</span><span class="sxs-lookup"><span data-stu-id="54666-108">DESCRIPTION</span></span>
<span data-ttu-id="54666-109">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrServicesProvider** pobiera informacje dotyczące dostawców usługi Azure Site Recovery w magazynie.</span><span class="sxs-lookup"><span data-stu-id="54666-109">The **Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="54666-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="54666-110">EXAMPLES</span></span>

### <span data-ttu-id="54666-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="54666-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="54666-112">Wyświetl listę wszystkich dostawców usług replikacji automatycznego odzyskiwania zarejestrowanych w magazynie usług Recovery Services odpowiadającym określonej sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="54666-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="54666-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="54666-113">PARAMETERS</span></span>

### <span data-ttu-id="54666-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54666-114">-DefaultProfile</span></span>
<span data-ttu-id="54666-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="54666-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="54666-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="54666-116">-Fabric</span></span>
<span data-ttu-id="54666-117">Określa obiekt sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="54666-117">Specifies the ASR fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54666-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="54666-118">-FriendlyName</span></span>
<span data-ttu-id="54666-119">Określa przyjazną nazwę dostawcy usług odzyskiwania ASR, z którego można uzyskać szczegółowe informacje.</span><span class="sxs-lookup"><span data-stu-id="54666-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="54666-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="54666-120">-Name</span></span>
<span data-ttu-id="54666-121">Określa nazwę dostawcy usług odzyskiwania ASR, do którego należy uzyskać szczegółowe informacje.</span><span class="sxs-lookup"><span data-stu-id="54666-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="54666-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54666-122">CommonParameters</span></span>
<span data-ttu-id="54666-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54666-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54666-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54666-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54666-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54666-125">INPUTS</span></span>

### <span data-ttu-id="54666-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="54666-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="54666-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="54666-127">OUTPUTS</span></span>

### <span data-ttu-id="54666-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="54666-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="54666-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="54666-129">NOTES</span></span>

## <span data-ttu-id="54666-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54666-130">RELATED LINKS</span></span>

[<span data-ttu-id="54666-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="54666-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="54666-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="54666-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
