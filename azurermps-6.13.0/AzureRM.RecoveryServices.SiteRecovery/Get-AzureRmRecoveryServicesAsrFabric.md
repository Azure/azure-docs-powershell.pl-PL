---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: db93d022d2abd6d3c6cecfe32b1f82be4483e850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548592"
---
# <span data-ttu-id="00a80-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="00a80-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="00a80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00a80-102">SYNOPSIS</span></span>
<span data-ttu-id="00a80-103">Zapoznaj się z informacjami na temat sieci szkieletowej odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="00a80-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00a80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00a80-104">SYNTAX</span></span>

### <span data-ttu-id="00a80-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="00a80-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00a80-106">ByName</span><span class="sxs-lookup"><span data-stu-id="00a80-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00a80-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="00a80-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00a80-108">Opis</span><span class="sxs-lookup"><span data-stu-id="00a80-108">DESCRIPTION</span></span>
<span data-ttu-id="00a80-109">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrFabric** pobiera właściwości określonej sieci szkieletowej odzyskiwania witryny platformy Azure lub całej sieci szkieletowej odzyskiwania witryny Azure w magazynie usługi odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="00a80-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="00a80-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00a80-110">EXAMPLES</span></span>

### <span data-ttu-id="00a80-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="00a80-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="00a80-112">Zwraca wszystkie materiały szkieletowe odzyskiwania witryny Azure w magazynie.</span><span class="sxs-lookup"><span data-stu-id="00a80-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="00a80-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="00a80-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="00a80-114">Zwracanie sieci szkieletowej odzyskiwania witryny Azure o nazwie xxxx.</span><span class="sxs-lookup"><span data-stu-id="00a80-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="00a80-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="00a80-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="00a80-116">Zwracanie sieci szkieletowej odzyskiwania witryny Azure o przyjaznej nazwie xxxx.</span><span class="sxs-lookup"><span data-stu-id="00a80-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="00a80-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00a80-117">PARAMETERS</span></span>

### <span data-ttu-id="00a80-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00a80-118">-DefaultProfile</span></span>
<span data-ttu-id="00a80-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="00a80-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00a80-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="00a80-120">-FriendlyName</span></span>
<span data-ttu-id="00a80-121">Wyszukiwanie w sieci szkieletowej ASR według przyjaznej nazwy sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="00a80-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="00a80-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="00a80-122">-Name</span></span>
<span data-ttu-id="00a80-123">Wyszukiwanie w sieci szkieletowej ASR według nazwy sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="00a80-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="00a80-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00a80-124">CommonParameters</span></span>
<span data-ttu-id="00a80-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00a80-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00a80-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00a80-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00a80-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00a80-127">INPUTS</span></span>

### <span data-ttu-id="00a80-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="00a80-128">None</span></span>

## <span data-ttu-id="00a80-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00a80-129">OUTPUTS</span></span>

### <span data-ttu-id="00a80-130">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="00a80-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="00a80-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00a80-131">NOTES</span></span>

## <span data-ttu-id="00a80-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00a80-132">RELATED LINKS</span></span>

[<span data-ttu-id="00a80-133">Nowe — AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="00a80-133">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="00a80-134">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="00a80-134">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)