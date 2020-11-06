---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: bd4280f87d397afdcab3f77e8305a0c1ff4b0ed2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542431"
---
# <span data-ttu-id="61e38-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="61e38-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="61e38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61e38-102">SYNOPSIS</span></span>
<span data-ttu-id="61e38-103">Pobiera zasady replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="61e38-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61e38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61e38-104">SYNTAX</span></span>

### <span data-ttu-id="61e38-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="61e38-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61e38-106">ByName</span><span class="sxs-lookup"><span data-stu-id="61e38-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61e38-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="61e38-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61e38-108">Opis</span><span class="sxs-lookup"><span data-stu-id="61e38-108">DESCRIPTION</span></span>
<span data-ttu-id="61e38-109">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrPolicy** pobiera listę skonfigurowanych zasad replikacji usługi Azure Site Recovery lub określonych zasad replikacji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="61e38-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="61e38-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61e38-110">EXAMPLES</span></span>

### <span data-ttu-id="61e38-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="61e38-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy
```

<span data-ttu-id="61e38-112">Retuns listy zasad replikacji</span><span class="sxs-lookup"><span data-stu-id="61e38-112">Retuns the list of replication policies</span></span>

### <span data-ttu-id="61e38-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="61e38-113">Example 2</span></span>
```
PS C:\>  Get-AzureRmRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="61e38-114">Retuns zasady replikacji z nazwą.</span><span class="sxs-lookup"><span data-stu-id="61e38-114">Retuns replication policy with name.</span></span>

### <span data-ttu-id="61e38-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="61e38-115">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="61e38-116">Zwraca zasady replikacji o określonej przyjaznej nazwie.</span><span class="sxs-lookup"><span data-stu-id="61e38-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="61e38-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61e38-117">PARAMETERS</span></span>

### <span data-ttu-id="61e38-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e38-118">-DefaultProfile</span></span>
<span data-ttu-id="61e38-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="61e38-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="61e38-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="61e38-120">-FriendlyName</span></span>
<span data-ttu-id="61e38-121">Określa przyjazną nazwę zasad replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="61e38-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="61e38-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="61e38-122">-Name</span></span>
<span data-ttu-id="61e38-123">Określa nazwę zasad replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="61e38-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="61e38-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e38-124">CommonParameters</span></span>
<span data-ttu-id="61e38-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61e38-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e38-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61e38-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e38-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61e38-127">INPUTS</span></span>

### <span data-ttu-id="61e38-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="61e38-128">None</span></span>

## <span data-ttu-id="61e38-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61e38-129">OUTPUTS</span></span>

### <span data-ttu-id="61e38-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="61e38-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="61e38-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61e38-131">NOTES</span></span>

## <span data-ttu-id="61e38-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61e38-132">RELATED LINKS</span></span>

[<span data-ttu-id="61e38-133">Nowe — AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="61e38-133">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="61e38-134">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="61e38-134">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
