---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a25375a565db8d2c69a423aa95033033de3f0f8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708703"
---
# <span data-ttu-id="0f34b-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="0f34b-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="0f34b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f34b-102">SYNOPSIS</span></span>
<span data-ttu-id="0f34b-103">Pobiera zasady replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="0f34b-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="0f34b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f34b-104">SYNTAX</span></span>

### <span data-ttu-id="0f34b-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="0f34b-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f34b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0f34b-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f34b-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="0f34b-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f34b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0f34b-108">DESCRIPTION</span></span>
<span data-ttu-id="0f34b-109">Polecenie cmdlet **Get-AzRecoveryServicesAsrPolicy** pobiera listę skonfigurowanych zasad replikacji usługi Azure Site Recovery lub określonych zasad replikacji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="0f34b-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="0f34b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f34b-110">EXAMPLES</span></span>

### <span data-ttu-id="0f34b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0f34b-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="0f34b-112">Retuns listy zasad replikacji</span><span class="sxs-lookup"><span data-stu-id="0f34b-112">Retuns the list of replication policies</span></span>

### <span data-ttu-id="0f34b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0f34b-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="0f34b-114">Retuns zasady replikacji z nazwą.</span><span class="sxs-lookup"><span data-stu-id="0f34b-114">Retuns replication policy with name.</span></span>

### <span data-ttu-id="0f34b-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0f34b-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="0f34b-116">Zwraca zasady replikacji o określonej przyjaznej nazwie.</span><span class="sxs-lookup"><span data-stu-id="0f34b-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="0f34b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f34b-117">PARAMETERS</span></span>

### <span data-ttu-id="0f34b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f34b-118">-DefaultProfile</span></span>
<span data-ttu-id="0f34b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f34b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0f34b-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0f34b-120">-FriendlyName</span></span>
<span data-ttu-id="0f34b-121">Określa przyjazną nazwę zasad replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="0f34b-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="0f34b-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0f34b-122">-Name</span></span>
<span data-ttu-id="0f34b-123">Określa nazwę zasad replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="0f34b-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="0f34b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f34b-124">CommonParameters</span></span>
<span data-ttu-id="0f34b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f34b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f34b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f34b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f34b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f34b-127">INPUTS</span></span>

### <span data-ttu-id="0f34b-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0f34b-128">None</span></span>

## <span data-ttu-id="0f34b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f34b-129">OUTPUTS</span></span>

### <span data-ttu-id="0f34b-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="0f34b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="0f34b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f34b-131">NOTES</span></span>

## <span data-ttu-id="0f34b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f34b-132">RELATED LINKS</span></span>

[<span data-ttu-id="0f34b-133">Nowe — AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="0f34b-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="0f34b-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="0f34b-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)