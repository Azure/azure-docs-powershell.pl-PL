---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
ms.openlocfilehash: c57b704f54eacbd9b5cac808e69f9bbf289dc0cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232755"
---
# <span data-ttu-id="d7a67-101">Stop-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="d7a67-101">Stop-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="d7a67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7a67-102">SYNOPSIS</span></span>
<span data-ttu-id="d7a67-103">Zatrzymuje operacje wystąpienia zarządzanego przez SQL.</span><span class="sxs-lookup"><span data-stu-id="d7a67-103">Stops a SQL managed instance's operations.</span></span>

## <span data-ttu-id="d7a67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7a67-104">SYNTAX</span></span>

### <span data-ttu-id="d7a67-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d7a67-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Default)</span></span>
```
Stop-AzSqlInstanceOperation [-Name] <String> [-ManagedInstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7a67-106">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7a67-106">StopByResourceIdParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7a67-107">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7a67-107">StopByInputObjectParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-InputObject] <AzureSqlManagedInstanceOperationModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7a67-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d7a67-108">DESCRIPTION</span></span>
<span data-ttu-id="d7a67-109">Polecenie cmdlet Stop-AzSqlInstanceOperation zatrzymuje działanie z podaną nazwą operacji w wystąpieniu zarządzanym SQL.</span><span class="sxs-lookup"><span data-stu-id="d7a67-109">The Stop-AzSqlInstanceOperation cmdlet stops operation with provided operation name on a SQL managed instance.</span></span>

## <span data-ttu-id="d7a67-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7a67-110">EXAMPLES</span></span>

### <span data-ttu-id="d7a67-111">Przykład 1. Aby uzyskać określoną operację</span><span class="sxs-lookup"><span data-stu-id="d7a67-111">Example 1: Get a specific operation</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name d0f5bef5-e2b1-4ef8-bb42-2e54073874f9

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:49:53 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="d7a67-112">To polecenie zatrzymuje działanie o nazwie "d0f5bef5-e2b1-4ef8-bb42-2e54073874f9" w wystąpieniu zarządzanym SQL.</span><span class="sxs-lookup"><span data-stu-id="d7a67-112">This command stops operation with name 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' on a SQL managed instance.</span></span>

### <span data-ttu-id="d7a67-113">Przykład 2: korzystanie z identyfikatora zasobu operacji</span><span class="sxs-lookup"><span data-stu-id="d7a67-113">Example 2: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 4253bf58-34f1-4499-80c6-198d94c659f7
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/4253bf58-34f1-4499-80c6-198d94c659f7
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 4253bf58-34f1-4499-80c6-198d94c659f7
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:47:32 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="d7a67-114">To polecenie zatrzymuje operację z identyfikatorem zasobu $managedInstanceOperation. ID.</span><span class="sxs-lookup"><span data-stu-id="d7a67-114">This command stops operation with resource id $managedInstanceOperation.Id.</span></span>

### <span data-ttu-id="d7a67-115">Przykład 3: korzystanie z obiektu Operation</span><span class="sxs-lookup"><span data-stu-id="d7a67-115">Example 3: Using operation object</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name b15a2b78-c42c-4e00-bf87-7ef4737552dc
PS C:\> Stop-AzSqlInstanceOperation -InputObject $managedInstanceOperation

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/b15a2b78-c42c-4e00-bf87-7ef4737552dc
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : b15a2b78-c42c-4e00-bf87-7ef4737552dc
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:44:57 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="d7a67-116">To polecenie zatrzymuje działanie w przypadku $managedInstanceOperation obiektów.</span><span class="sxs-lookup"><span data-stu-id="d7a67-116">This command stops operation with object $managedInstanceOperation.</span></span>

## <span data-ttu-id="d7a67-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7a67-117">PARAMETERS</span></span>

### <span data-ttu-id="d7a67-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7a67-118">-DefaultProfile</span></span>
<span data-ttu-id="d7a67-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7a67-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7a67-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d7a67-120">-Force</span></span>
<span data-ttu-id="d7a67-121">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="d7a67-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d7a67-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d7a67-122">-InputObject</span></span>
<span data-ttu-id="d7a67-123">Operacja anulowania</span><span class="sxs-lookup"><span data-stu-id="d7a67-123">The operation to cancel</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel
Parameter Sets: StopByInputObjectParameterSet
Aliases: SqlInstanceOperation

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7a67-124">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="d7a67-124">-ManagedInstanceName</span></span>
<span data-ttu-id="d7a67-125">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="d7a67-125">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7a67-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d7a67-126">-Name</span></span>
<span data-ttu-id="d7a67-127">Nazwa operacji.</span><span class="sxs-lookup"><span data-stu-id="d7a67-127">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases: OperationName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7a67-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7a67-128">-ResourceGroupName</span></span>
<span data-ttu-id="d7a67-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d7a67-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7a67-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7a67-130">-ResourceId</span></span>
<span data-ttu-id="d7a67-131">Obiekt identyfikator zasobu do zatrzymania</span><span class="sxs-lookup"><span data-stu-id="d7a67-131">The resource id of operation object to stop</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7a67-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7a67-132">-Confirm</span></span>
<span data-ttu-id="d7a67-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7a67-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7a67-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7a67-134">-WhatIf</span></span>
<span data-ttu-id="d7a67-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7a67-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7a67-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7a67-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7a67-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7a67-137">CommonParameters</span></span>
<span data-ttu-id="d7a67-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7a67-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7a67-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7a67-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7a67-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7a67-140">INPUTS</span></span>

### <span data-ttu-id="d7a67-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d7a67-141">System.String</span></span>

### <span data-ttu-id="d7a67-142">Microsoft. Azure. Commands. SQL. ManagedInstanceOperation. model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="d7a67-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="d7a67-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7a67-143">OUTPUTS</span></span>

### <span data-ttu-id="d7a67-144">Microsoft. Azure. Commands. SQL. ManagedInstanceOperation. model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="d7a67-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="d7a67-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7a67-145">NOTES</span></span>

## <span data-ttu-id="d7a67-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7a67-146">RELATED LINKS</span></span>
