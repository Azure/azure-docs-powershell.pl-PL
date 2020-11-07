---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: 9d63c208daffe6e06da759ff929de120cab58c1c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704897"
---
# <span data-ttu-id="0d96d-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="0d96d-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="0d96d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d96d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d96d-103">Usuwa definicję rejestracji.</span><span class="sxs-lookup"><span data-stu-id="0d96d-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="0d96d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d96d-104">SYNTAX</span></span>

### <span data-ttu-id="0d96d-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="0d96d-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition -Id <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d96d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0d96d-106">ByResourceId</span></span>
```
Remove-AzManagedServicesDefinition -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d96d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0d96d-107">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d96d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0d96d-108">DESCRIPTION</span></span>
<span data-ttu-id="0d96d-109">Usuwa definicję rejestracji.</span><span class="sxs-lookup"><span data-stu-id="0d96d-109">Deletes the registration definition.</span></span>

## <span data-ttu-id="0d96d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d96d-110">EXAMPLES</span></span>

### <span data-ttu-id="0d96d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0d96d-111">Example 1</span></span>
```powershell
PS C:\> Remove-RegistrationDefinition -Id 0513b566-cab0-4fef-9b53-a285cd33389f
```

<span data-ttu-id="0d96d-112">Usuwa definicję rejestracji o danym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="0d96d-112">Removes the registration definition given it identifier.</span></span>

### <span data-ttu-id="0d96d-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0d96d-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzManagedServicesDefinition -ResourceId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/11b7c937-c5c1-4dd1-9a77-204591f93fcd

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
11b7c937-c5c1-4dd1-9a77-204591f93fcd bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="0d96d-114">Usuwa definicję rejestracji z pełnym kwalifikowanym identyfikatorem zasobu.</span><span class="sxs-lookup"><span data-stu-id="0d96d-114">Removes the registration definition given the fully qualified resource id.</span></span> 

### <span data-ttu-id="0d96d-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0d96d-115">Example 3</span></span>
```powershell
PS C:\> $def = New-AzManagedServicesDefinition -RegistrationDefinitionName 572e1807-b80b-4401-9128-1968f432a5ad -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7"
PS C:\> Remove-AzManagedServicesDefinition -InputObject $def

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
eee59839-119f-453f-adec-4a72a8687125 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="0d96d-116">Usuwa definicję rejestracji danego obiektu.</span><span class="sxs-lookup"><span data-stu-id="0d96d-116">Deletes the registration definition given the object.</span></span>

## <span data-ttu-id="0d96d-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d96d-117">PARAMETERS</span></span>

### <span data-ttu-id="0d96d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d96d-118">-AsJob</span></span>
<span data-ttu-id="0d96d-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0d96d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d96d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d96d-120">-DefaultProfile</span></span>
<span data-ttu-id="0d96d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d96d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d96d-122">-ID</span><span class="sxs-lookup"><span data-stu-id="0d96d-122">-Id</span></span>
<span data-ttu-id="0d96d-123">Identyfikator definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="0d96d-123">The registration definition identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d96d-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0d96d-124">-InputObject</span></span>
<span data-ttu-id="0d96d-125">Obiekt definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="0d96d-125">The registration definition object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d96d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d96d-126">-ResourceId</span></span>
<span data-ttu-id="0d96d-127">Identyfikator zasobu definicji rejestracji</span><span class="sxs-lookup"><span data-stu-id="0d96d-127">ResourceId of the registration definition</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d96d-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0d96d-128">-Confirm</span></span>
<span data-ttu-id="0d96d-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d96d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d96d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d96d-130">-WhatIf</span></span>
<span data-ttu-id="0d96d-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d96d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d96d-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0d96d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d96d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d96d-133">CommonParameters</span></span>
<span data-ttu-id="0d96d-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d96d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d96d-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d96d-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d96d-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d96d-136">INPUTS</span></span>

### <span data-ttu-id="0d96d-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0d96d-137">None</span></span>

## <span data-ttu-id="0d96d-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d96d-138">OUTPUTS</span></span>

### <span data-ttu-id="0d96d-139">Microsoft. Azure. PowerShell. polecenia. ManagedServices. models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="0d96d-139">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="0d96d-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d96d-140">NOTES</span></span>

## <span data-ttu-id="0d96d-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d96d-141">RELATED LINKS</span></span>
