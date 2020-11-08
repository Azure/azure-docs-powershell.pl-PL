---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
ms.openlocfilehash: 1f165177871a2d8b425829dddaef6d1f0298cfb4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222510"
---
# <span data-ttu-id="ca8a0-101">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ca8a0-101">New-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="ca8a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca8a0-102">SYNOPSIS</span></span>
<span data-ttu-id="ca8a0-103">Tworzy nową tożsamość użytkownika o przypisanej tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

## <span data-ttu-id="ca8a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca8a0-104">SYNTAX</span></span>

```
New-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca8a0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ca8a0-105">DESCRIPTION</span></span>
<span data-ttu-id="ca8a0-106">Polecenie cmdlet **New-AzUserAssignedIdentity** powoduje utworzenie nowej tożsamości przypisanej do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-106">The **New-AzUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="ca8a0-107">Gdy jest używana z już istniejącą tożsamością, zaktualizowała tożsamość.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="ca8a0-108">Aby dodać znaczniki Menedżera zasobów platformy Azure do tożsamości, użyj polecenia cmdlet Set-AzResource.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-108">To add Azure Resource Manager tags to the identity, please use the Set-AzResource cmdlet.</span></span>

## <span data-ttu-id="ca8a0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca8a0-109">EXAMPLES</span></span>

### <span data-ttu-id="ca8a0-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ca8a0-110">Example 1</span></span>
<span data-ttu-id="ca8a0-111">Ten przykładowy polecenie cmdlet tworzy nowy przypisany użytkownikowi tożsamość o nazwie **ID1** w grupie zasób **PSRG** w lokalizacji grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

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

### <span data-ttu-id="ca8a0-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ca8a0-112">Example 2</span></span>
<span data-ttu-id="ca8a0-113">Ten przykładowy polecenie cmdlet tworzy nowy przypisany użytkownikowi tożsamość o nazwie **ID1** pod pozycją Grupa zasobów **PSRG** w regionie zachód.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

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

## <span data-ttu-id="ca8a0-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca8a0-114">PARAMETERS</span></span>

### <span data-ttu-id="ca8a0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca8a0-115">-AsJob</span></span>
<span data-ttu-id="ca8a0-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ca8a0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca8a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca8a0-117">-DefaultProfile</span></span>
<span data-ttu-id="ca8a0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca8a0-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ca8a0-119">-Location</span></span>
<span data-ttu-id="ca8a0-120">Nazwa regionu platformy Azure, w którym ma zostać utworzona tożsamość.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-120">The Azure region name where the Identity should be created.</span></span>

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

### <span data-ttu-id="ca8a0-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ca8a0-121">-Name</span></span>
<span data-ttu-id="ca8a0-122">Nazwa tożsamości.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-122">The Identity name.</span></span>

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

### <span data-ttu-id="ca8a0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca8a0-123">-ResourceGroupName</span></span>
<span data-ttu-id="ca8a0-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-124">The resource group name.</span></span>

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

### <span data-ttu-id="ca8a0-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="ca8a0-125">-Tag</span></span>
<span data-ttu-id="ca8a0-126">Znaczniki Menedżera zasobów platformy Azure skojarzone z tożsamością.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-126">The Azure Resource Manager tags associated with the identity.</span></span>

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

### <span data-ttu-id="ca8a0-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca8a0-127">-Confirm</span></span>
<span data-ttu-id="ca8a0-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca8a0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca8a0-129">-WhatIf</span></span>
<span data-ttu-id="ca8a0-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca8a0-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca8a0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca8a0-132">CommonParameters</span></span>
<span data-ttu-id="ca8a0-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca8a0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca8a0-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca8a0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca8a0-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca8a0-135">INPUTS</span></span>

### <span data-ttu-id="ca8a0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ca8a0-136">System.String</span></span>

### <span data-ttu-id="ca8a0-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ca8a0-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ca8a0-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca8a0-138">OUTPUTS</span></span>

### <span data-ttu-id="ca8a0-139">Microsoft. Azure. Commands. ManagedServiceIdentity. models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ca8a0-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="ca8a0-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca8a0-140">NOTES</span></span>

## <span data-ttu-id="ca8a0-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca8a0-141">RELATED LINKS</span></span>
