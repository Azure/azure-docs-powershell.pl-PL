---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: c3bd5ecf7e3561be5f9e6b8d990c40281135982c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222987"
---
# <span data-ttu-id="520a3-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="520a3-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="520a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="520a3-102">SYNOPSIS</span></span>
<span data-ttu-id="520a3-103">Zapoznaj się z informacjami na temat sieci szkieletowej odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="520a3-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="520a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="520a3-104">SYNTAX</span></span>

### <span data-ttu-id="520a3-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="520a3-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="520a3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="520a3-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="520a3-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="520a3-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="520a3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="520a3-108">DESCRIPTION</span></span>
<span data-ttu-id="520a3-109">Polecenie cmdlet **Get-AzRecoveryServicesAsrFabric** pobiera właściwości określonej sieci szkieletowej odzyskiwania witryny platformy Azure lub całej sieci szkieletowej odzyskiwania witryny Azure w magazynie usługi odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="520a3-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="520a3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="520a3-110">EXAMPLES</span></span>

### <span data-ttu-id="520a3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="520a3-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="520a3-112">Zwraca wszystkie materiały szkieletowe odzyskiwania witryny Azure w magazynie.</span><span class="sxs-lookup"><span data-stu-id="520a3-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="520a3-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="520a3-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="520a3-114">Zwracanie sieci szkieletowej odzyskiwania witryny Azure o nazwie xxxx.</span><span class="sxs-lookup"><span data-stu-id="520a3-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="520a3-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="520a3-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="520a3-116">Zwracanie sieci szkieletowej odzyskiwania witryny Azure o przyjaznej nazwie xxxx.</span><span class="sxs-lookup"><span data-stu-id="520a3-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="520a3-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="520a3-117">PARAMETERS</span></span>

### <span data-ttu-id="520a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="520a3-118">-DefaultProfile</span></span>
<span data-ttu-id="520a3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="520a3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="520a3-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="520a3-120">-FriendlyName</span></span>
<span data-ttu-id="520a3-121">Wyszukiwanie w sieci szkieletowej ASR według przyjaznej nazwy sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="520a3-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="520a3-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="520a3-122">-Name</span></span>
<span data-ttu-id="520a3-123">Wyszukiwanie w sieci szkieletowej ASR według nazwy sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="520a3-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="520a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="520a3-124">CommonParameters</span></span>
<span data-ttu-id="520a3-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="520a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="520a3-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="520a3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="520a3-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="520a3-127">INPUTS</span></span>

### <span data-ttu-id="520a3-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="520a3-128">None</span></span>

## <span data-ttu-id="520a3-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="520a3-129">OUTPUTS</span></span>

### <span data-ttu-id="520a3-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="520a3-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="520a3-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="520a3-131">NOTES</span></span>

## <span data-ttu-id="520a3-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="520a3-132">RELATED LINKS</span></span>

[<span data-ttu-id="520a3-133">Nowe — AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="520a3-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="520a3-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="520a3-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
