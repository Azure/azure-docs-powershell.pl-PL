---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 4be24acddf1f02ecd9216a06690958feed2d6c57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049574"
---
# <span data-ttu-id="8ee6e-101">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8ee6e-101">Get-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="8ee6e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ee6e-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee6e-103">Umożliwia wyświetlenie szczegółów dotyczących dostawców usług odzyskiwania ASR zarejestrowanych w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="8ee6e-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

## <span data-ttu-id="8ee6e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ee6e-104">SYNTAX</span></span>

### <span data-ttu-id="8ee6e-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="8ee6e-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ee6e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8ee6e-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ee6e-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8ee6e-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ee6e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8ee6e-108">DESCRIPTION</span></span>
<span data-ttu-id="8ee6e-109">Polecenie cmdlet **Get-AzRecoveryServicesAsrServicesProvider** pobiera informacje dotyczące dostawców usługi Azure Site Recovery w magazynie.</span><span class="sxs-lookup"><span data-stu-id="8ee6e-109">The **Get-AzRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="8ee6e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ee6e-110">EXAMPLES</span></span>

### <span data-ttu-id="8ee6e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8ee6e-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzRecoveryServicesAsrFabric | Get-AzRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="8ee6e-112">Wyświetl listę wszystkich dostawców usług replikacji automatycznego odzyskiwania zarejestrowanych w magazynie usług Recovery Services odpowiadającym określonej sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="8ee6e-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="8ee6e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ee6e-113">PARAMETERS</span></span>

### <span data-ttu-id="8ee6e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ee6e-114">-DefaultProfile</span></span>
<span data-ttu-id="8ee6e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ee6e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee6e-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="8ee6e-116">-Fabric</span></span>
<span data-ttu-id="8ee6e-117">Określa obiekt sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="8ee6e-117">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="8ee6e-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8ee6e-118">-FriendlyName</span></span>
<span data-ttu-id="8ee6e-119">Określa przyjazną nazwę dostawcy usług odzyskiwania ASR, z którego można uzyskać szczegółowe informacje.</span><span class="sxs-lookup"><span data-stu-id="8ee6e-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="8ee6e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8ee6e-120">-Name</span></span>
<span data-ttu-id="8ee6e-121">Określa nazwę dostawcy usług odzyskiwania ASR, do którego należy uzyskać szczegółowe informacje.</span><span class="sxs-lookup"><span data-stu-id="8ee6e-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="8ee6e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee6e-122">CommonParameters</span></span>
<span data-ttu-id="8ee6e-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ee6e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee6e-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ee6e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee6e-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ee6e-125">INPUTS</span></span>

### <span data-ttu-id="8ee6e-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="8ee6e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="8ee6e-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ee6e-127">OUTPUTS</span></span>

### <span data-ttu-id="8ee6e-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8ee6e-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="8ee6e-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ee6e-129">NOTES</span></span>

## <span data-ttu-id="8ee6e-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ee6e-130">RELATED LINKS</span></span>

[<span data-ttu-id="8ee6e-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8ee6e-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="8ee6e-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8ee6e-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
