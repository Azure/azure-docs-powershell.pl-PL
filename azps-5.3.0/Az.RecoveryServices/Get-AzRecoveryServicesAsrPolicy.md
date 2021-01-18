---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a7cd359714be965c232019310ac2f2abfe0fe233
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501394"
---
# <span data-ttu-id="f6cab-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f6cab-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="f6cab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6cab-102">SYNOPSIS</span></span>
<span data-ttu-id="f6cab-103">Pobiera zasady replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="f6cab-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="f6cab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6cab-104">SYNTAX</span></span>

### <span data-ttu-id="f6cab-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f6cab-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6cab-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f6cab-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6cab-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f6cab-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6cab-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f6cab-108">DESCRIPTION</span></span>
<span data-ttu-id="f6cab-109">Polecenie cmdlet **Get-AzRecoveryServicesAsrPolicy** pobiera listę skonfigurowanych zasad replikacji usługi Azure Site Recovery lub określonych zasad replikacji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="f6cab-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="f6cab-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6cab-110">EXAMPLES</span></span>

### <span data-ttu-id="f6cab-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f6cab-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="f6cab-112">Zwraca listę zasad replikacji.</span><span class="sxs-lookup"><span data-stu-id="f6cab-112">Returns the list of replication policies</span></span>

### <span data-ttu-id="f6cab-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f6cab-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="f6cab-114">Zwraca zasady replikacji o nazwie.</span><span class="sxs-lookup"><span data-stu-id="f6cab-114">Returns replication policy with name.</span></span>

### <span data-ttu-id="f6cab-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f6cab-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="f6cab-116">Zwraca zasady replikacji o określonej przyjaznej nazwie.</span><span class="sxs-lookup"><span data-stu-id="f6cab-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="f6cab-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6cab-117">PARAMETERS</span></span>

### <span data-ttu-id="f6cab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6cab-118">-DefaultProfile</span></span>
<span data-ttu-id="f6cab-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6cab-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f6cab-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f6cab-120">-FriendlyName</span></span>
<span data-ttu-id="f6cab-121">Określa przyjazną nazwę zasad replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="f6cab-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="f6cab-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f6cab-122">-Name</span></span>
<span data-ttu-id="f6cab-123">Określa nazwę zasad replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="f6cab-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="f6cab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6cab-124">CommonParameters</span></span>
<span data-ttu-id="f6cab-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6cab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6cab-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6cab-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6cab-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6cab-127">INPUTS</span></span>

### <span data-ttu-id="f6cab-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f6cab-128">None</span></span>

## <span data-ttu-id="f6cab-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6cab-129">OUTPUTS</span></span>

### <span data-ttu-id="f6cab-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="f6cab-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="f6cab-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6cab-131">NOTES</span></span>

## <span data-ttu-id="f6cab-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6cab-132">RELATED LINKS</span></span>

[<span data-ttu-id="f6cab-133">Nowe — AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f6cab-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="f6cab-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f6cab-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
