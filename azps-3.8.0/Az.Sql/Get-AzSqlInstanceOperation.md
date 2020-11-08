---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
ms.openlocfilehash: b9f008d610729d1f1bc73affbb5b8f3eae04ecdd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053225"
---
# <span data-ttu-id="e43a2-101">Get-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="e43a2-101">Get-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="e43a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e43a2-102">SYNOPSIS</span></span>
<span data-ttu-id="e43a2-103">Pobiera operacje wystąpienia zarządzanego przez SQL.</span><span class="sxs-lookup"><span data-stu-id="e43a2-103">Gets a SQL managed instance's operations.</span></span>

## <span data-ttu-id="e43a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e43a2-104">SYNTAX</span></span>

### <span data-ttu-id="e43a2-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e43a2-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceOperation [-Name <Guid>] -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e43a2-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="e43a2-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstanceOperation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e43a2-107">ListByManagedInstanceParameterSet</span><span class="sxs-lookup"><span data-stu-id="e43a2-107">ListByManagedInstanceParameterSet</span></span>
```
Get-AzSqlInstanceOperation -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e43a2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e43a2-108">DESCRIPTION</span></span>
<span data-ttu-id="e43a2-109">Polecenie cmdlet Get-AzSqlInstanceOperation pobiera informacje o operacjach w wystąpieniu zarządzanym SQL.</span><span class="sxs-lookup"><span data-stu-id="e43a2-109">The Get-AzSqlInstanceOperation cmdlet gets information about the operations on a SQL managed instance.</span></span> <span data-ttu-id="e43a2-110">Możesz wyświetlić wszystkie operacje w zarządzanym wystąpieniu lub wyświetlić określoną operację, podając nazwę operacji.</span><span class="sxs-lookup"><span data-stu-id="e43a2-110">You can view all operations on a managed instance or view a specific operation by providing the operation name.</span></span>

## <span data-ttu-id="e43a2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e43a2-111">EXAMPLES</span></span>

### <span data-ttu-id="e43a2-112">Przykład 1. Pobierz wszystkie operacje wystąpienia</span><span class="sxs-lookup"><span data-stu-id="e43a2-112">Example 1: Get all instance's operations</span></span>
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
```

<span data-ttu-id="e43a2-113">To polecenie pobiera wszystkie operacje wystąpienia zarządzanego przez SQL.</span><span class="sxs-lookup"><span data-stu-id="e43a2-113">This command gets all operations a SQL managed instance.</span></span>

### <span data-ttu-id="e43a2-114">Przykład 2: uzyskiwanie określonej operacji</span><span class="sxs-lookup"><span data-stu-id="e43a2-114">Example 2: Get a specific operation</span></span>
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
```

<span data-ttu-id="e43a2-115">To polecenie pobiera operację o nazwie "5870c6d8-6703-4b27-8ae4-687b4ca7caea" w wystąpieniu zarządzanym SQL.</span><span class="sxs-lookup"><span data-stu-id="e43a2-115">This command gets operation with name '5870c6d8-6703-4b27-8ae4-687b4ca7caea' on a SQL managed instance.</span></span>

### <span data-ttu-id="e43a2-116">Przykład 3: korzystanie z identyfikatora zasobu operacji</span><span class="sxs-lookup"><span data-stu-id="e43a2-116">Example 3: Using operation resource id</span></span>
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
```

<span data-ttu-id="e43a2-117">To polecenie pobiera operację z identyfikatorem "/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea".</span><span class="sxs-lookup"><span data-stu-id="e43a2-117">This command gets operation with id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span></span>

## <span data-ttu-id="e43a2-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e43a2-118">PARAMETERS</span></span>

### <span data-ttu-id="e43a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e43a2-119">-DefaultProfile</span></span>
<span data-ttu-id="e43a2-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e43a2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e43a2-121">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="e43a2-121">-ManagedInstanceName</span></span>
<span data-ttu-id="e43a2-122">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="e43a2-122">The name of the instance.</span></span>

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

### <span data-ttu-id="e43a2-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e43a2-123">-Name</span></span>
<span data-ttu-id="e43a2-124">Nazwa operacji.</span><span class="sxs-lookup"><span data-stu-id="e43a2-124">The name of the operation.</span></span>

```yaml
Type: System.Guid
Parameter Sets: DefaultParameterSet
Aliases: OperationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43a2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e43a2-125">-ResourceGroupName</span></span>
<span data-ttu-id="e43a2-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e43a2-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="e43a2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e43a2-127">-ResourceId</span></span>
<span data-ttu-id="e43a2-128">Identyfikator zasobu operacji wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="e43a2-128">The managed instance operation resource identifier.</span></span>

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

### <span data-ttu-id="e43a2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e43a2-129">CommonParameters</span></span>
<span data-ttu-id="e43a2-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e43a2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e43a2-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e43a2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e43a2-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e43a2-132">INPUTS</span></span>

### <span data-ttu-id="e43a2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e43a2-133">System.String</span></span>

## <span data-ttu-id="e43a2-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e43a2-134">OUTPUTS</span></span>

### <span data-ttu-id="e43a2-135">Microsoft. Azure. Commands. SQL. ManagedInstanceOperation. model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="e43a2-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="e43a2-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e43a2-136">NOTES</span></span>

## <span data-ttu-id="e43a2-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e43a2-137">RELATED LINKS</span></span>
