---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 42c2fa289eef04734c0619ca7bf2a46ece19606e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008401"
---
# <span data-ttu-id="0077a-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="0077a-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="0077a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0077a-102">SYNOPSIS</span></span>
<span data-ttu-id="0077a-103">Anuluje usługę ponownego odtwarzania dziennika, upuszczając bazę danych.</span><span class="sxs-lookup"><span data-stu-id="0077a-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="0077a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0077a-104">SYNTAX</span></span>

### <span data-ttu-id="0077a-105">LogReplayInstanceDatabaseFromInputParameters (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="0077a-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0077a-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="0077a-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0077a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0077a-107">DESCRIPTION</span></span>
<span data-ttu-id="0077a-108">Polecenie **cmdlet Stop-AzSqlInstanceDatabaseLogReplay** usunie bazę danych, co oznacza anulowanie usługi ponownego odtwarzania dziennika.</span><span class="sxs-lookup"><span data-stu-id="0077a-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="0077a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0077a-109">EXAMPLES</span></span>

### <span data-ttu-id="0077a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0077a-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="0077a-111">To polecenie anuluje usługę ponownego odtwarzania dziennika w danej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="0077a-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="0077a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0077a-112">PARAMETERS</span></span>

### <span data-ttu-id="0077a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0077a-113">-DefaultProfile</span></span>
<span data-ttu-id="0077a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0077a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0077a-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0077a-115">-Force</span></span>
<span data-ttu-id="0077a-116">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="0077a-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0077a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0077a-117">-InputObject</span></span>
<span data-ttu-id="0077a-118">Obiekt bazy danych wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="0077a-118">The instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0077a-119">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0077a-119">-InstanceName</span></span>
<span data-ttu-id="0077a-120">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="0077a-120">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0077a-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0077a-121">-Name</span></span>
<span data-ttu-id="0077a-122">Nazwa bazy danych wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="0077a-122">The name of the instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0077a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0077a-123">-PassThru</span></span>
<span data-ttu-id="0077a-124">Określa, czy grupa synchronizacji ma być zwracana.</span><span class="sxs-lookup"><span data-stu-id="0077a-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="0077a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0077a-125">-ResourceGroupName</span></span>
<span data-ttu-id="0077a-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0077a-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0077a-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0077a-127">-Confirm</span></span>
<span data-ttu-id="0077a-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0077a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0077a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0077a-129">-WhatIf</span></span>
<span data-ttu-id="0077a-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0077a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0077a-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0077a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0077a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0077a-132">CommonParameters</span></span>
<span data-ttu-id="0077a-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0077a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0077a-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0077a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0077a-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0077a-135">INPUTS</span></span>

### <span data-ttu-id="0077a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0077a-136">System.String</span></span>

### <span data-ttu-id="0077a-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0077a-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="0077a-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0077a-138">OUTPUTS</span></span>

### <span data-ttu-id="0077a-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0077a-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="0077a-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0077a-140">NOTES</span></span>

## <span data-ttu-id="0077a-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0077a-141">RELATED LINKS</span></span>
