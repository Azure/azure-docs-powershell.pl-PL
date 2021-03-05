---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 0638e44f9f1c8febcbb9700fce1b9c4c9d5e410c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014561"
---
# <span data-ttu-id="ee761-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ee761-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="ee761-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee761-102">SYNOPSIS</span></span>
<span data-ttu-id="ee761-103">Pobiera informacje o administratorze usługi Azure AD dla wystąpienia zarządzanego przez sql.</span><span class="sxs-lookup"><span data-stu-id="ee761-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="ee761-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ee761-104">SYNTAX</span></span>

### <span data-ttu-id="ee761-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="ee761-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee761-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee761-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee761-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee761-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee761-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ee761-108">DESCRIPTION</span></span>
<span data-ttu-id="ee761-109">Polecenie **cmdlet Get-AzSqlInstanceActiveDirectoryAdministrator** pobiera informacje o administratorze usługi Azure Active Directory (Azure AD) dla wystąpienia zarządzanego AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ee761-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="ee761-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ee761-110">EXAMPLES</span></span>

### <span data-ttu-id="ee761-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ee761-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="ee761-112">To polecenie pobiera informacje o administratorze usługi Azure AD dla zarządzanego wystąpienia o nazwie ManagedInstance01 skojarzonego z grupą zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ee761-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="ee761-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ee761-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="ee761-114">To polecenie pobiera informacje o administratorze usługi Azure AD z obiektu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="ee761-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="ee761-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ee761-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="ee761-116">To polecenie pobiera informacje o administratorze usługi Azure AD przy użyciu identyfikatora zasobu zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ee761-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="ee761-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee761-117">PARAMETERS</span></span>

### <span data-ttu-id="ee761-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee761-118">-DefaultProfile</span></span>
<span data-ttu-id="ee761-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee761-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee761-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee761-120">-InputObject</span></span>
<span data-ttu-id="ee761-121">Obiekt zarządzanego wystąpienia do użycia.</span><span class="sxs-lookup"><span data-stu-id="ee761-121">The managed instance object to use.</span></span>

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

### <span data-ttu-id="ee761-122">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ee761-122">-InstanceName</span></span>
<span data-ttu-id="ee761-123">Nazwa zarządzanego wystąpienia języka SQL.</span><span class="sxs-lookup"><span data-stu-id="ee761-123">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="ee761-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee761-124">-ResourceGroupName</span></span>
<span data-ttu-id="ee761-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ee761-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="ee761-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee761-126">-ResourceId</span></span>
<span data-ttu-id="ee761-127">Identyfikator zasobu wystąpienia do użycia</span><span class="sxs-lookup"><span data-stu-id="ee761-127">The resource id of instance to use</span></span>

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

### <span data-ttu-id="ee761-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee761-128">CommonParameters</span></span>
<span data-ttu-id="ee761-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee761-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee761-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee761-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee761-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee761-131">INPUTS</span></span>

### <span data-ttu-id="ee761-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ee761-132">System.String</span></span>

## <span data-ttu-id="ee761-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee761-133">OUTPUTS</span></span>

### <span data-ttu-id="ee761-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="ee761-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="ee761-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ee761-135">NOTES</span></span>

## <span data-ttu-id="ee761-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee761-136">RELATED LINKS</span></span>

[<span data-ttu-id="ee761-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ee761-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="ee761-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ee761-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
