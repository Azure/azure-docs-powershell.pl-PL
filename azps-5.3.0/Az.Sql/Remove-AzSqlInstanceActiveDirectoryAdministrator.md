---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 361517912166c9548ecc69358c6dd0e776cfcd3a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374535"
---
# <span data-ttu-id="bdc4e-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="bdc4e-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="bdc4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bdc4e-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc4e-103">Umożliwia usunięcie wystąpienia zarządzanego przez SQL administratora usługi Azure AD.</span><span class="sxs-lookup"><span data-stu-id="bdc4e-103">Removes an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="bdc4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bdc4e-104">SYNTAX</span></span>

### <span data-ttu-id="bdc4e-105">UseResourceGroupAndInstanceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bdc4e-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdc4e-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdc4e-106">UseInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru]
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdc4e-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdc4e-107">UserResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdc4e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bdc4e-108">DESCRIPTION</span></span>
<span data-ttu-id="bdc4e-109">Polecenie cmdlet **Remove-AzSqlInstanceActiveDirectoryAdministrator** usuwa administratora usługi Azure Active Directory (Azure AD) dla AzureSQL zarządzanego wystąpienia w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bdc4e-109">The **Remove-AzSqlInstanceActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="bdc4e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bdc4e-110">EXAMPLES</span></span>

### <span data-ttu-id="bdc4e-111">Przykład 1: usuwanie administratora</span><span class="sxs-lookup"><span data-stu-id="bdc4e-111">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstanceName01" -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="bdc4e-112">To polecenie usuwa administratora usługi Azure AD dla wystąpienia zarządzanego o nazwie ManagedInstanceName01 skojarzonego z grupą zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="bdc4e-112">This command removes the Azure AD administrator for the managed instance named ManagedInstanceName01 associated with the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="bdc4e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bdc4e-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="bdc4e-114">To polecenie usuwa administratora usługi Azure AD z obiektu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="bdc4e-114">This command removes the Azure AD administrator from the managed instance object.</span></span>

### <span data-ttu-id="bdc4e-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="bdc4e-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="bdc4e-116">To polecenie usuwa administratora usługi Azure AD przy użyciu identyfikatora zasobu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="bdc4e-116">This command removes the Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="bdc4e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bdc4e-117">PARAMETERS</span></span>

### <span data-ttu-id="bdc4e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc4e-118">-DefaultProfile</span></span>
<span data-ttu-id="bdc4e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc4e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdc4e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bdc4e-120">-Force</span></span>
<span data-ttu-id="bdc4e-121">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="bdc4e-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="bdc4e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bdc4e-122">-InputObject</span></span>
<span data-ttu-id="bdc4e-123">Obiekt wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="bdc4e-123">The managed instance object to use.</span></span>

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

### <span data-ttu-id="bdc4e-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="bdc4e-124">-InstanceName</span></span>
<span data-ttu-id="bdc4e-125">Nazwa wystąpienia zarządzanego SQL.</span><span class="sxs-lookup"><span data-stu-id="bdc4e-125">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="bdc4e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdc4e-126">-PassThru</span></span>
<span data-ttu-id="bdc4e-127">Określa, czy ma zostać zwrócone usuniętego administratora usługi AD.</span><span class="sxs-lookup"><span data-stu-id="bdc4e-127">Defines whether to return the removed AD administrator</span></span>

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

### <span data-ttu-id="bdc4e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc4e-128">-ResourceGroupName</span></span>
<span data-ttu-id="bdc4e-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bdc4e-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="bdc4e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdc4e-130">-ResourceId</span></span>
<span data-ttu-id="bdc4e-131">Identyfikator zasobu, którego należy użyć</span><span class="sxs-lookup"><span data-stu-id="bdc4e-131">The resource id of instance to use</span></span>

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

### <span data-ttu-id="bdc4e-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdc4e-132">-Confirm</span></span>
<span data-ttu-id="bdc4e-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdc4e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdc4e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdc4e-134">-WhatIf</span></span>
<span data-ttu-id="bdc4e-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdc4e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdc4e-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bdc4e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdc4e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc4e-137">CommonParameters</span></span>
<span data-ttu-id="bdc4e-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdc4e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc4e-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdc4e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc4e-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdc4e-140">INPUTS</span></span>

### <span data-ttu-id="bdc4e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bdc4e-141">System.String</span></span>

## <span data-ttu-id="bdc4e-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bdc4e-142">OUTPUTS</span></span>

### <span data-ttu-id="bdc4e-143">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryAdministrator. model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="bdc4e-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="bdc4e-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bdc4e-144">NOTES</span></span>

## <span data-ttu-id="bdc4e-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdc4e-145">RELATED LINKS</span></span>

[<span data-ttu-id="bdc4e-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="bdc4e-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="bdc4e-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="bdc4e-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)
