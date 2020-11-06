---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/get-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Get-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Get-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 4d28b91ec4f05b39c6e348aff17bbb1bec1a2dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545647"
---
# <span data-ttu-id="328f0-101">Get-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="328f0-101">Get-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="328f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="328f0-102">SYNOPSIS</span></span>
<span data-ttu-id="328f0-103">Pobiera tożsamość/tożsamości przypisane do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="328f0-103">Gets User Assigned Identity/identities.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="328f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="328f0-104">SYNTAX</span></span>

### <span data-ttu-id="328f0-105">SuscriptionParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="328f0-105">SuscriptionParameterSet (Default)</span></span>
```
Get-AzureRmUserAssignedIdentity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="328f0-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="328f0-106">ResourceGroupParameterSet</span></span>
```
Get-AzureRmUserAssignedIdentity -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="328f0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="328f0-107">DESCRIPTION</span></span>
<span data-ttu-id="328f0-108">**AzureRmUserAssignedIdentity** pobiera istniejące tożsamości przypisane użytkownikowi.</span><span class="sxs-lookup"><span data-stu-id="328f0-108">The **Get-AzureRmUserAssignedIdentity** gets existing user assigned identities.</span></span>

## <span data-ttu-id="328f0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="328f0-109">EXAMPLES</span></span>

### <span data-ttu-id="328f0-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="328f0-110">Example 1</span></span>
<span data-ttu-id="328f0-111">Ten przykładowy polecenie cmdlet pobiera tożsamość przydzieloną użytkownikowi o nazwie **ID1** pod grupą zasobów **PSRG**</span><span class="sxs-lookup"><span data-stu-id="328f0-111">This example cmdlet gets the User Assigned Identity with name **ID1** under the resource group **PSRG**</span></span>

```powershell
PS C:\> Get-AzureRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="328f0-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="328f0-112">Example 2</span></span>
<span data-ttu-id="328f0-113">Ten przykładowy polecenie cmdlet pobiera wszystkie tożsamości przypisane do użytkownika pod pozycją Grupa zasobów **PSRG**</span><span class="sxs-lookup"><span data-stu-id="328f0-113">This example cmdlet gets all the User Assigned Identities under the resource group **PSRG**</span></span>

```powershell
PS C:\> Get-AzureRmUserAssignedIdentity -ResourceGroupName PSRG

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2

ResourceGroupName : PSRG

Name              : ID2

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="328f0-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="328f0-114">Example 3</span></span>
<span data-ttu-id="328f0-115">Ten przykładowy polecenie cmdlet pobiera wszystkie tożsamości przypisane do użytkownika w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="328f0-115">This example cmdlet gets all the User Assigned Identities under the subscription.</span></span>

```powershell
PS C:\> Get-AzureRmUserAssignedIdentity

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2

ResourceGroupName : PSRG

Name              : ID2

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG2/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG2

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG2/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="328f0-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="328f0-116">PARAMETERS</span></span>

### <span data-ttu-id="328f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="328f0-117">-DefaultProfile</span></span>
<span data-ttu-id="328f0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="328f0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="328f0-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="328f0-119">-Name</span></span>
<span data-ttu-id="328f0-120">Nazwa tożsamości.</span><span class="sxs-lookup"><span data-stu-id="328f0-120">The Identity name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="328f0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="328f0-121">-ResourceGroupName</span></span>
<span data-ttu-id="328f0-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="328f0-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="328f0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="328f0-123">CommonParameters</span></span>
<span data-ttu-id="328f0-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="328f0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="328f0-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="328f0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="328f0-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="328f0-126">INPUTS</span></span>

### <span data-ttu-id="328f0-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="328f0-127">None</span></span>

## <span data-ttu-id="328f0-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="328f0-128">OUTPUTS</span></span>

### <span data-ttu-id="328f0-129">Microsoft. Azure. Commands. ManagedServiceIdentity. models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="328f0-129">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="328f0-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="328f0-130">NOTES</span></span>

## <span data-ttu-id="328f0-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="328f0-131">RELATED LINKS</span></span>
