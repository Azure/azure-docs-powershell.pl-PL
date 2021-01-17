---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2a7c74c4c8fef61e01ccbbb512ff428b9e885f06
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346093"
---
# <span data-ttu-id="ee4ef-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="ee4ef-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="ee4ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee4ef-102">SYNOPSIS</span></span>
<span data-ttu-id="ee4ef-103">Anuluje usługę rejestrowania powtarzania, upuszczając bazę danych.</span><span class="sxs-lookup"><span data-stu-id="ee4ef-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="ee4ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee4ef-104">SYNTAX</span></span>

### <span data-ttu-id="ee4ef-105">LogReplayInstanceDatabaseFromInputParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ee4ef-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee4ef-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="ee4ef-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee4ef-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ee4ef-107">DESCRIPTION</span></span>
<span data-ttu-id="ee4ef-108">Polecenie cmdlet **stop-AzSqlInstanceDatabaseLogReplay** odrzuca bazę danych i w związku z tym anuluje usługę powtarzania dziennika.</span><span class="sxs-lookup"><span data-stu-id="ee4ef-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="ee4ef-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee4ef-109">EXAMPLES</span></span>

### <span data-ttu-id="ee4ef-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ee4ef-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="ee4ef-111">To polecenie spowoduje anulowanie usługi powtarzania dziennika w danej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="ee4ef-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="ee4ef-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee4ef-112">PARAMETERS</span></span>

### <span data-ttu-id="ee4ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee4ef-113">-DefaultProfile</span></span>
<span data-ttu-id="ee4ef-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee4ef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee4ef-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ee4ef-115">-Force</span></span>
<span data-ttu-id="ee4ef-116">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="ee4ef-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ee4ef-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ee4ef-117">-InputObject</span></span>
<span data-ttu-id="ee4ef-118">Obiekt bazy danych wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ee4ef-118">The instance database object.</span></span>

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

### <span data-ttu-id="ee4ef-119">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ee4ef-119">-InstanceName</span></span>
<span data-ttu-id="ee4ef-120">Nazwa wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ee4ef-120">The name of the instance.</span></span>

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

### <span data-ttu-id="ee4ef-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ee4ef-121">-Name</span></span>
<span data-ttu-id="ee4ef-122">Nazwa bazy danych wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ee4ef-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="ee4ef-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee4ef-123">-PassThru</span></span>
<span data-ttu-id="ee4ef-124">Określa, czy ma być zwracana Grupa synchronizacja.</span><span class="sxs-lookup"><span data-stu-id="ee4ef-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="ee4ef-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee4ef-125">-ResourceGroupName</span></span>
<span data-ttu-id="ee4ef-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ee4ef-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="ee4ef-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ee4ef-127">-Confirm</span></span>
<span data-ttu-id="ee4ef-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee4ef-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee4ef-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee4ef-129">-WhatIf</span></span>
<span data-ttu-id="ee4ef-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee4ef-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee4ef-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ee4ef-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee4ef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee4ef-132">CommonParameters</span></span>
<span data-ttu-id="ee4ef-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee4ef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee4ef-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee4ef-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee4ef-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee4ef-135">INPUTS</span></span>

### <span data-ttu-id="ee4ef-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ee4ef-136">System.String</span></span>

### <span data-ttu-id="ee4ef-137">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ee4ef-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="ee4ef-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee4ef-138">OUTPUTS</span></span>

### <span data-ttu-id="ee4ef-139">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ee4ef-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="ee4ef-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee4ef-140">NOTES</span></span>

## <span data-ttu-id="ee4ef-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee4ef-141">RELATED LINKS</span></span>
