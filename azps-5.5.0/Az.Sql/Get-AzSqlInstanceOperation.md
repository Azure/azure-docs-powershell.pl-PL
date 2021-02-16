---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
ms.openlocfilehash: a190e6a47c0a3027505c471be870c10ac80593cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183315"
---
# <span data-ttu-id="748ba-101">Get-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="748ba-101">Get-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="748ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="748ba-102">SYNOPSIS</span></span>
<span data-ttu-id="748ba-103">Pobiera operacje na wystąpieniu zarządzanym przez język SQL.</span><span class="sxs-lookup"><span data-stu-id="748ba-103">Gets a SQL managed instance's operations.</span></span>

## <span data-ttu-id="748ba-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="748ba-104">SYNTAX</span></span>

### <span data-ttu-id="748ba-105">DefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="748ba-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceOperation [-Name <String>] -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="748ba-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="748ba-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstanceOperation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="748ba-107">ListByManagedInstanceParameterSet</span><span class="sxs-lookup"><span data-stu-id="748ba-107">ListByManagedInstanceParameterSet</span></span>
```
Get-AzSqlInstanceOperation -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="748ba-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="748ba-108">DESCRIPTION</span></span>
<span data-ttu-id="748ba-109">Polecenie Get-AzSqlInstanceOperation pobiera informacje o operacjach w wystąpieniu zarządzanym przez język SQL.</span><span class="sxs-lookup"><span data-stu-id="748ba-109">The Get-AzSqlInstanceOperation cmdlet gets information about the operations on a SQL managed instance.</span></span> <span data-ttu-id="748ba-110">Możesz wyświetlić wszystkie operacje w zarządzanym wystąpieniu lub wyświetlić określoną operację, podając nazwę operacji.</span><span class="sxs-lookup"><span data-stu-id="748ba-110">You can view all operations on a managed instance or view a specific operation by providing the operation name.</span></span>

## <span data-ttu-id="748ba-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="748ba-111">EXAMPLES</span></span>

### <span data-ttu-id="748ba-112">Przykład 1. Uzyskiwanie wszystkich operacji wystąpienia</span><span class="sxs-lookup"><span data-stu-id="748ba-112">Example 1: Get all instance's operations</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/79f2c91b-0080-4c14-b9b4-d9991c6e82dd
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 79f2c91b-0080-4c14-b9b4-d9991c6e82dd
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:19:53 AM
State                   : Cancelled
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="748ba-113">To polecenie pobiera wszystkie operacje jako wystąpienie zarządzane przez język SQL.</span><span class="sxs-lookup"><span data-stu-id="748ba-113">This command gets all operations a SQL managed instance.</span></span>

### <span data-ttu-id="748ba-114">Przykład 2. Uzyskiwanie konkretnej operacji</span><span class="sxs-lookup"><span data-stu-id="748ba-114">Example 2: Get a specific operation</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="748ba-115">To polecenie działa z nazwą "5870c6d8-6703-4b27-8ae4-687b4ca7caea" w wystąpieniu zarządzanym przez język SQL.</span><span class="sxs-lookup"><span data-stu-id="748ba-115">This command gets operation with name '5870c6d8-6703-4b27-8ae4-687b4ca7caea' on a SQL managed instance.</span></span>

### <span data-ttu-id="748ba-116">Przykład 3. Korzystanie z identyfikatora zasobu operacji</span><span class="sxs-lookup"><span data-stu-id="748ba-116">Example 3: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="748ba-117">To polecenie działa z identyfikatorem '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span><span class="sxs-lookup"><span data-stu-id="748ba-117">This command gets operation with id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span></span>

## <span data-ttu-id="748ba-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="748ba-118">PARAMETERS</span></span>

### <span data-ttu-id="748ba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="748ba-119">-DefaultProfile</span></span>
<span data-ttu-id="748ba-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="748ba-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="748ba-121">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="748ba-121">-ManagedInstanceName</span></span>
<span data-ttu-id="748ba-122">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="748ba-122">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="748ba-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="748ba-123">-Name</span></span>
<span data-ttu-id="748ba-124">Nazwa operacji.</span><span class="sxs-lookup"><span data-stu-id="748ba-124">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: OperationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="748ba-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="748ba-125">-ResourceGroupName</span></span>
<span data-ttu-id="748ba-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="748ba-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="748ba-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="748ba-127">-ResourceId</span></span>
<span data-ttu-id="748ba-128">Identyfikator zasobu operacji zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="748ba-128">The managed instance operation resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByManagedInstanceOperationResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="748ba-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="748ba-129">CommonParameters</span></span>
<span data-ttu-id="748ba-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="748ba-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="748ba-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="748ba-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="748ba-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="748ba-132">INPUTS</span></span>

### <span data-ttu-id="748ba-133">System.String</span><span class="sxs-lookup"><span data-stu-id="748ba-133">System.String</span></span>

## <span data-ttu-id="748ba-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="748ba-134">OUTPUTS</span></span>

### <span data-ttu-id="748ba-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="748ba-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="748ba-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="748ba-136">NOTES</span></span>

## <span data-ttu-id="748ba-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="748ba-137">RELATED LINKS</span></span>
