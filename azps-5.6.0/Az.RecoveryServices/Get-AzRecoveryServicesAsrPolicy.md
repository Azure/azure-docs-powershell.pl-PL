---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: e9559993e122e5b713228630b3b783b1f0e6a981
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005841"
---
# <span data-ttu-id="25e41-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="25e41-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="25e41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25e41-102">SYNOPSIS</span></span>
<span data-ttu-id="25e41-103">Pobiera zasady replikacji asr.</span><span class="sxs-lookup"><span data-stu-id="25e41-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="25e41-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="25e41-104">SYNTAX</span></span>

### <span data-ttu-id="25e41-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="25e41-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25e41-106">ByName</span><span class="sxs-lookup"><span data-stu-id="25e41-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25e41-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="25e41-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25e41-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="25e41-108">DESCRIPTION</span></span>
<span data-ttu-id="25e41-109">Polecenie **cmdlet Get-AzRecoveryServicesAsrPolicy** pobiera listę skonfigurowanych zasad replikacji usługi Azure Site Recovery lub określonych zasad replikacji według nazw.</span><span class="sxs-lookup"><span data-stu-id="25e41-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="25e41-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="25e41-110">EXAMPLES</span></span>

### <span data-ttu-id="25e41-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="25e41-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="25e41-112">Zwraca listę zasad replikacji.</span><span class="sxs-lookup"><span data-stu-id="25e41-112">Returns the list of replication policies</span></span>

### <span data-ttu-id="25e41-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="25e41-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="25e41-114">Zwraca zasady replikacji z nazwą.</span><span class="sxs-lookup"><span data-stu-id="25e41-114">Returns replication policy with name.</span></span>

### <span data-ttu-id="25e41-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="25e41-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="25e41-116">Zwraca zasady replikacji o określonej przyjaznej nazwie.</span><span class="sxs-lookup"><span data-stu-id="25e41-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="25e41-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25e41-117">PARAMETERS</span></span>

### <span data-ttu-id="25e41-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e41-118">-DefaultProfile</span></span>
<span data-ttu-id="25e41-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="25e41-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="25e41-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="25e41-120">-FriendlyName</span></span>
<span data-ttu-id="25e41-121">Określa przyjazną nazwę zasad replikacji asr.</span><span class="sxs-lookup"><span data-stu-id="25e41-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="25e41-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="25e41-122">-Name</span></span>
<span data-ttu-id="25e41-123">Określa nazwę zasad replikacji asr.</span><span class="sxs-lookup"><span data-stu-id="25e41-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="25e41-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e41-124">CommonParameters</span></span>
<span data-ttu-id="25e41-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25e41-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e41-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25e41-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e41-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25e41-127">INPUTS</span></span>

### <span data-ttu-id="25e41-128">Brak</span><span class="sxs-lookup"><span data-stu-id="25e41-128">None</span></span>

## <span data-ttu-id="25e41-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25e41-129">OUTPUTS</span></span>

### <span data-ttu-id="25e41-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="25e41-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="25e41-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="25e41-131">NOTES</span></span>

## <span data-ttu-id="25e41-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25e41-132">RELATED LINKS</span></span>

[<span data-ttu-id="25e41-133">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="25e41-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="25e41-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="25e41-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
