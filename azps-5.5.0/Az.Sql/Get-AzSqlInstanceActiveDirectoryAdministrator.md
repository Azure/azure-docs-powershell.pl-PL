---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 90dade6f8ae40d007e7f5dc575c954b1d4ad639f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191075"
---
# <span data-ttu-id="7d8d2-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7d8d2-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="7d8d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d8d2-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8d2-103">Pobiera informacje o administratorze usługi Azure AD dla wystąpienia zarządzanego przez sql.</span><span class="sxs-lookup"><span data-stu-id="7d8d2-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="7d8d2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7d8d2-104">SYNTAX</span></span>

### <span data-ttu-id="7d8d2-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="7d8d2-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d8d2-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d8d2-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d8d2-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d8d2-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d8d2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7d8d2-108">DESCRIPTION</span></span>
<span data-ttu-id="7d8d2-109">Polecenie cmdlet **Get-AzSqlInstanceActiveDirectoryAdministrator** pobiera informacje o administratorze usługi Azure Active Directory (Azure AD) dla wystąpienia zarządzanego AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7d8d2-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="7d8d2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7d8d2-110">EXAMPLES</span></span>

### <span data-ttu-id="7d8d2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7d8d2-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="7d8d2-112">To polecenie pobiera informacje o administratorze usługi Azure AD dla zarządzanego wystąpienia o nazwie ManagedInstance01 skojarzonego z grupą zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="7d8d2-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="7d8d2-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7d8d2-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="7d8d2-114">To polecenie pobiera informacje o administratorze usługi Azure AD z obiektu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="7d8d2-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="7d8d2-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="7d8d2-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="7d8d2-116">To polecenie pobiera informacje o administratorze usługi Azure AD przy użyciu identyfikatora zasobu zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="7d8d2-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="7d8d2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d8d2-117">PARAMETERS</span></span>

### <span data-ttu-id="7d8d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8d2-118">-DefaultProfile</span></span>
<span data-ttu-id="7d8d2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8d2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d8d2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d8d2-120">-InputObject</span></span>
<span data-ttu-id="7d8d2-121">Obiekt zarządzanego wystąpienia do użycia.</span><span class="sxs-lookup"><span data-stu-id="7d8d2-121">The managed instance object to use.</span></span>

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

### <span data-ttu-id="7d8d2-122">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7d8d2-122">-InstanceName</span></span>
<span data-ttu-id="7d8d2-123">Nazwa zarządzanego wystąpienia języka SQL.</span><span class="sxs-lookup"><span data-stu-id="7d8d2-123">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="7d8d2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d8d2-124">-ResourceGroupName</span></span>
<span data-ttu-id="7d8d2-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7d8d2-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="7d8d2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d8d2-126">-ResourceId</span></span>
<span data-ttu-id="7d8d2-127">Identyfikator zasobu wystąpienia do użycia</span><span class="sxs-lookup"><span data-stu-id="7d8d2-127">The resource id of instance to use</span></span>

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

### <span data-ttu-id="7d8d2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8d2-128">CommonParameters</span></span>
<span data-ttu-id="7d8d2-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d8d2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8d2-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d8d2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8d2-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d8d2-131">INPUTS</span></span>

### <span data-ttu-id="7d8d2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7d8d2-132">System.String</span></span>

## <span data-ttu-id="7d8d2-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d8d2-133">OUTPUTS</span></span>

### <span data-ttu-id="7d8d2-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="7d8d2-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="7d8d2-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7d8d2-135">NOTES</span></span>

## <span data-ttu-id="7d8d2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d8d2-136">RELATED LINKS</span></span>

[<span data-ttu-id="7d8d2-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7d8d2-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="7d8d2-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7d8d2-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
