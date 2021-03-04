---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/powershell/module/az.managedserviceidentity/new-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
ms.openlocfilehash: 1c4395c4e2c36fd07fee6345c1a5ff7d724b7c0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975745"
---
# <span data-ttu-id="cdee7-101">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="cdee7-101">New-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="cdee7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdee7-102">SYNOPSIS</span></span>
<span data-ttu-id="cdee7-103">Tworzy nową tożsamość przypisaną do użytkownika lub aktualizuje istniejącą tożsamość przypisaną przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cdee7-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

## <span data-ttu-id="cdee7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cdee7-104">SYNTAX</span></span>

```
New-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdee7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cdee7-105">DESCRIPTION</span></span>
<span data-ttu-id="cdee7-106">Polecenie **cmdlet New-AzUserAssignedIdentity** tworzy nową tożsamość przypisaną do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cdee7-106">The **New-AzUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="cdee7-107">W przypadku korzystania z istniejącej tożsamości zaktualizowano ją.</span><span class="sxs-lookup"><span data-stu-id="cdee7-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="cdee7-108">Aby dodać tagi usługi Azure Resource Manager do tożsamości, użyj Set-AzResource cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdee7-108">To add Azure Resource Manager tags to the identity, please use the Set-AzResource cmdlet.</span></span>

## <span data-ttu-id="cdee7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cdee7-109">EXAMPLES</span></span>

### <span data-ttu-id="cdee7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cdee7-110">Example 1</span></span>
<span data-ttu-id="cdee7-111">W tym przykładzie polecenie cmdlet tworzy nową tożsamość przypisaną przez użytkownika o nazwie **ID1** w grupie zasobów **PSRG** w lokalizacji grupy Zasobów.</span><span class="sxs-lookup"><span data-stu-id="cdee7-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : centralus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="cdee7-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cdee7-112">Example 2</span></span>
<span data-ttu-id="cdee7-113">W tym przykładzie polecenie cmdlet tworzy nową tożsamość przypisaną do użytkownika o nazwie **ID1** w grupie zasobów **PSRG** w regionie zachód.</span><span class="sxs-lookup"><span data-stu-id="cdee7-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1 -Location westus

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

## <span data-ttu-id="cdee7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdee7-114">PARAMETERS</span></span>

### <span data-ttu-id="cdee7-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="cdee7-115">-AsJob</span></span>
<span data-ttu-id="cdee7-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cdee7-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdee7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdee7-117">-DefaultProfile</span></span>
<span data-ttu-id="cdee7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cdee7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdee7-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cdee7-119">-Location</span></span>
<span data-ttu-id="cdee7-120">Nazwa regionu platformy Azure, w którym powinna zostać utworzona tożsamość.</span><span class="sxs-lookup"><span data-stu-id="cdee7-120">The Azure region name where the Identity should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdee7-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cdee7-121">-Name</span></span>
<span data-ttu-id="cdee7-122">Nazwa tożsamości.</span><span class="sxs-lookup"><span data-stu-id="cdee7-122">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdee7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdee7-123">-ResourceGroupName</span></span>
<span data-ttu-id="cdee7-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cdee7-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdee7-125">— Tag</span><span class="sxs-lookup"><span data-stu-id="cdee7-125">-Tag</span></span>
<span data-ttu-id="cdee7-126">Tagi usługi Azure Resource Manager skojarzone z tożsamością.</span><span class="sxs-lookup"><span data-stu-id="cdee7-126">The Azure Resource Manager tags associated with the identity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdee7-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cdee7-127">-Confirm</span></span>
<span data-ttu-id="cdee7-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cdee7-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdee7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdee7-129">-WhatIf</span></span>
<span data-ttu-id="cdee7-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdee7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdee7-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cdee7-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdee7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdee7-132">CommonParameters</span></span>
<span data-ttu-id="cdee7-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdee7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdee7-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdee7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdee7-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdee7-135">INPUTS</span></span>

### <span data-ttu-id="cdee7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="cdee7-136">System.String</span></span>

### <span data-ttu-id="cdee7-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="cdee7-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cdee7-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdee7-138">OUTPUTS</span></span>

### <span data-ttu-id="cdee7-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="cdee7-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="cdee7-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cdee7-140">NOTES</span></span>

## <span data-ttu-id="cdee7-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdee7-141">RELATED LINKS</span></span>
