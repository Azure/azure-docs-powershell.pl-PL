---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 16a2250941ba0e28d40648ed2cd69fee7ffefc8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955146"
---
# <span data-ttu-id="319f0-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="319f0-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="319f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="319f0-102">SYNOPSIS</span></span>
<span data-ttu-id="319f0-103">Usuwa administratora usługi Azure AD dla wystąpienia zarządzanego przez sql.</span><span class="sxs-lookup"><span data-stu-id="319f0-103">Removes an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="319f0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="319f0-104">SYNTAX</span></span>

### <span data-ttu-id="319f0-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="319f0-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="319f0-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="319f0-106">UseInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru]
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="319f0-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="319f0-107">UserResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="319f0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="319f0-108">DESCRIPTION</span></span>
<span data-ttu-id="319f0-109">Polecenie cmdlet **Remove-AzSqlInstanceActiveDirectoryAdministrator** usuwa administratora usługi Azure Active Directory (Azure AD) dla wystąpienia zarządzanego AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="319f0-109">The **Remove-AzSqlInstanceActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="319f0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="319f0-110">EXAMPLES</span></span>

### <span data-ttu-id="319f0-111">Przykład 1. Usuwanie administratora</span><span class="sxs-lookup"><span data-stu-id="319f0-111">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstanceName01" -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="319f0-112">To polecenie usuwa administratora usługi Azure AD dla zarządzanego wystąpienia o nazwie ManagedInstanceName01 skojarzonego z grupą zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="319f0-112">This command removes the Azure AD administrator for the managed instance named ManagedInstanceName01 associated with the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="319f0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="319f0-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="319f0-114">To polecenie usuwa administratora usługi Azure AD z obiektu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="319f0-114">This command removes the Azure AD administrator from the managed instance object.</span></span>

### <span data-ttu-id="319f0-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="319f0-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="319f0-116">To polecenie usuwa administratora usługi Azure AD przy użyciu identyfikatora zasobu zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="319f0-116">This command removes the Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="319f0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="319f0-117">PARAMETERS</span></span>

### <span data-ttu-id="319f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="319f0-118">-DefaultProfile</span></span>
<span data-ttu-id="319f0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="319f0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="319f0-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="319f0-120">-Force</span></span>
<span data-ttu-id="319f0-121">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="319f0-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="319f0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="319f0-122">-InputObject</span></span>
<span data-ttu-id="319f0-123">Obiekt zarządzanego wystąpienia do użycia.</span><span class="sxs-lookup"><span data-stu-id="319f0-123">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="319f0-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="319f0-124">-InstanceName</span></span>
<span data-ttu-id="319f0-125">Nazwa zarządzanego wystąpienia języka SQL.</span><span class="sxs-lookup"><span data-stu-id="319f0-125">SQL Managed Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319f0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="319f0-126">-PassThru</span></span>
<span data-ttu-id="319f0-127">Określa, czy usunięty administrator usługi AD ma zostać zwrócony</span><span class="sxs-lookup"><span data-stu-id="319f0-127">Defines whether to return the removed AD administrator</span></span>

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

### <span data-ttu-id="319f0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="319f0-128">-ResourceGroupName</span></span>
<span data-ttu-id="319f0-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="319f0-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319f0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="319f0-130">-ResourceId</span></span>
<span data-ttu-id="319f0-131">Identyfikator zasobu wystąpienia do użycia</span><span class="sxs-lookup"><span data-stu-id="319f0-131">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319f0-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="319f0-132">-Confirm</span></span>
<span data-ttu-id="319f0-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="319f0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="319f0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="319f0-134">-WhatIf</span></span>
<span data-ttu-id="319f0-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="319f0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="319f0-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="319f0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="319f0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="319f0-137">CommonParameters</span></span>
<span data-ttu-id="319f0-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="319f0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="319f0-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="319f0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="319f0-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="319f0-140">INPUTS</span></span>

### <span data-ttu-id="319f0-141">System.String</span><span class="sxs-lookup"><span data-stu-id="319f0-141">System.String</span></span>

## <span data-ttu-id="319f0-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="319f0-142">OUTPUTS</span></span>

### <span data-ttu-id="319f0-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="319f0-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="319f0-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="319f0-144">NOTES</span></span>

## <span data-ttu-id="319f0-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="319f0-145">RELATED LINKS</span></span>

[<span data-ttu-id="319f0-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="319f0-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="319f0-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="319f0-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)
