---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 90dade6f8ae40d007e7f5dc575c954b1d4ad639f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053255"
---
# <span data-ttu-id="e0802-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e0802-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="e0802-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0802-102">SYNOPSIS</span></span>
<span data-ttu-id="e0802-103">Pobiera informacje o administratorze usługi Azure AD dla wystąpienia zarządzanego SQL.</span><span class="sxs-lookup"><span data-stu-id="e0802-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="e0802-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0802-104">SYNTAX</span></span>

### <span data-ttu-id="e0802-105">UseResourceGroupAndInstanceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e0802-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0802-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0802-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0802-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0802-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0802-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e0802-108">DESCRIPTION</span></span>
<span data-ttu-id="e0802-109">Polecenie cmdlet **Get-AzSqlInstanceActiveDirectoryAdministrator** pobiera informacje o administratorze usługi Azure Active Directory (Azure AD) dla AzureSQL zarządzanego wystąpienia w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e0802-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="e0802-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0802-110">EXAMPLES</span></span>

### <span data-ttu-id="e0802-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e0802-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="e0802-112">To polecenie pobiera informacje o administratorze usługi Azure AD dla wystąpienia zarządzanego o nazwie ManagedInstance01, które jest skojarzone z grupą zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="e0802-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="e0802-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e0802-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="e0802-114">To polecenie pobiera informacje o administratorze usługi Azure AD z obiektu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="e0802-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="e0802-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e0802-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="e0802-116">To polecenie pobiera informacje o administratorze usługi Azure AD przy użyciu identyfikatora zasobu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="e0802-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="e0802-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0802-117">PARAMETERS</span></span>

### <span data-ttu-id="e0802-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0802-118">-DefaultProfile</span></span>
<span data-ttu-id="e0802-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0802-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0802-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e0802-120">-InputObject</span></span>
<span data-ttu-id="e0802-121">Obiekt wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="e0802-121">The managed instance object to use.</span></span>

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

### <span data-ttu-id="e0802-122">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e0802-122">-InstanceName</span></span>
<span data-ttu-id="e0802-123">Nazwa wystąpienia zarządzanego SQL.</span><span class="sxs-lookup"><span data-stu-id="e0802-123">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="e0802-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0802-124">-ResourceGroupName</span></span>
<span data-ttu-id="e0802-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0802-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="e0802-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0802-126">-ResourceId</span></span>
<span data-ttu-id="e0802-127">Identyfikator zasobu, którego należy użyć</span><span class="sxs-lookup"><span data-stu-id="e0802-127">The resource id of instance to use</span></span>

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

### <span data-ttu-id="e0802-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0802-128">CommonParameters</span></span>
<span data-ttu-id="e0802-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0802-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0802-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0802-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0802-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0802-131">INPUTS</span></span>

### <span data-ttu-id="e0802-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e0802-132">System.String</span></span>

## <span data-ttu-id="e0802-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0802-133">OUTPUTS</span></span>

### <span data-ttu-id="e0802-134">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryAdministrator. model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="e0802-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="e0802-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0802-135">NOTES</span></span>

## <span data-ttu-id="e0802-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0802-136">RELATED LINKS</span></span>

[<span data-ttu-id="e0802-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e0802-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="e0802-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e0802-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
