---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
ms.openlocfilehash: a190e6a47c0a3027505c471be870c10ac80593cd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499822"
---
# <span data-ttu-id="b848c-101">Get-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="b848c-101">Get-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="b848c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b848c-102">SYNOPSIS</span></span>
<span data-ttu-id="b848c-103">Pobiera operacje wystąpienia zarządzanego przez SQL.</span><span class="sxs-lookup"><span data-stu-id="b848c-103">Gets a SQL managed instance's operations.</span></span>

## <span data-ttu-id="b848c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b848c-104">SYNTAX</span></span>

### <span data-ttu-id="b848c-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b848c-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceOperation [-Name <String>] -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b848c-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="b848c-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstanceOperation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b848c-107">ListByManagedInstanceParameterSet</span><span class="sxs-lookup"><span data-stu-id="b848c-107">ListByManagedInstanceParameterSet</span></span>
```
Get-AzSqlInstanceOperation -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b848c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b848c-108">DESCRIPTION</span></span>
<span data-ttu-id="b848c-109">Polecenie cmdlet Get-AzSqlInstanceOperation pobiera informacje o operacjach w wystąpieniu zarządzanym SQL.</span><span class="sxs-lookup"><span data-stu-id="b848c-109">The Get-AzSqlInstanceOperation cmdlet gets information about the operations on a SQL managed instance.</span></span> <span data-ttu-id="b848c-110">Możesz wyświetlić wszystkie operacje w zarządzanym wystąpieniu lub wyświetlić określoną operację, podając nazwę operacji.</span><span class="sxs-lookup"><span data-stu-id="b848c-110">You can view all operations on a managed instance or view a specific operation by providing the operation name.</span></span>

## <span data-ttu-id="b848c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b848c-111">EXAMPLES</span></span>

### <span data-ttu-id="b848c-112">Przykład 1. Pobierz wszystkie operacje wystąpienia</span><span class="sxs-lookup"><span data-stu-id="b848c-112">Example 1: Get all instance's operations</span></span>
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

<span data-ttu-id="b848c-113">To polecenie pobiera wszystkie operacje wystąpienia zarządzanego przez SQL.</span><span class="sxs-lookup"><span data-stu-id="b848c-113">This command gets all operations a SQL managed instance.</span></span>

### <span data-ttu-id="b848c-114">Przykład 2: uzyskiwanie określonej operacji</span><span class="sxs-lookup"><span data-stu-id="b848c-114">Example 2: Get a specific operation</span></span>
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

<span data-ttu-id="b848c-115">To polecenie pobiera operację o nazwie "5870c6d8-6703-4b27-8ae4-687b4ca7caea" w wystąpieniu zarządzanym SQL.</span><span class="sxs-lookup"><span data-stu-id="b848c-115">This command gets operation with name '5870c6d8-6703-4b27-8ae4-687b4ca7caea' on a SQL managed instance.</span></span>

### <span data-ttu-id="b848c-116">Przykład 3: korzystanie z identyfikatora zasobu operacji</span><span class="sxs-lookup"><span data-stu-id="b848c-116">Example 3: Using operation resource id</span></span>
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

<span data-ttu-id="b848c-117">To polecenie pobiera operację z identyfikatorem "/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea".</span><span class="sxs-lookup"><span data-stu-id="b848c-117">This command gets operation with id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span></span>

## <span data-ttu-id="b848c-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b848c-118">PARAMETERS</span></span>

### <span data-ttu-id="b848c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b848c-119">-DefaultProfile</span></span>
<span data-ttu-id="b848c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b848c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b848c-121">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="b848c-121">-ManagedInstanceName</span></span>
<span data-ttu-id="b848c-122">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="b848c-122">The name of the instance.</span></span>

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

### <span data-ttu-id="b848c-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b848c-123">-Name</span></span>
<span data-ttu-id="b848c-124">Nazwa operacji.</span><span class="sxs-lookup"><span data-stu-id="b848c-124">The name of the operation.</span></span>

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

### <span data-ttu-id="b848c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b848c-125">-ResourceGroupName</span></span>
<span data-ttu-id="b848c-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b848c-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="b848c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b848c-127">-ResourceId</span></span>
<span data-ttu-id="b848c-128">Identyfikator zasobu operacji wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="b848c-128">The managed instance operation resource identifier.</span></span>

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

### <span data-ttu-id="b848c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b848c-129">CommonParameters</span></span>
<span data-ttu-id="b848c-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b848c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b848c-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b848c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b848c-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b848c-132">INPUTS</span></span>

### <span data-ttu-id="b848c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b848c-133">System.String</span></span>

## <span data-ttu-id="b848c-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b848c-134">OUTPUTS</span></span>

### <span data-ttu-id="b848c-135">Microsoft. Azure. Commands. SQL. ManagedInstanceOperation. model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="b848c-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="b848c-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b848c-136">NOTES</span></span>

## <span data-ttu-id="b848c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b848c-137">RELATED LINKS</span></span>
