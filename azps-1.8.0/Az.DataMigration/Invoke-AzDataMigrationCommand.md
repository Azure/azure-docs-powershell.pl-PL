---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: f00c1499e7f7e8a5a6d6b14bcbd8289b35ae2ced
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868471"
---
# <span data-ttu-id="ea55f-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="ea55f-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="ea55f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea55f-102">SYNOPSIS</span></span>
<span data-ttu-id="ea55f-103">Tworzy nowe polecenie do wykonania na istniejącym zadaniu DMS.</span><span class="sxs-lookup"><span data-stu-id="ea55f-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="ea55f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea55f-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="ea55f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ea55f-105">DESCRIPTION</span></span>
<span data-ttu-id="ea55f-106">Polecenie cmdlet Invoke-AzDataMigrationCommand tworzy nowe zadanie w celu uruchomienia go w istniejącym zadaniu migracji.</span><span class="sxs-lookup"><span data-stu-id="ea55f-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="ea55f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea55f-107">EXAMPLES</span></span>

### <span data-ttu-id="ea55f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ea55f-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="ea55f-109">W powyższych przykładach użyto polecenia cmdlet Invoke-AzDataMigrationCommand, aby utworzyć polecenie dla istniejącej usługi, projektu i zadania.</span><span class="sxs-lookup"><span data-stu-id="ea55f-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="ea55f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea55f-110">PARAMETERS</span></span>

### <span data-ttu-id="ea55f-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="ea55f-111">-CommandType</span></span>
<span data-ttu-id="ea55f-112">Typ polecenia.</span><span class="sxs-lookup"><span data-stu-id="ea55f-112">Command Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.CommandTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: CompleteSqlDBSync, CancelMongoDB, RestartMongoDB, FinishMongoDB, CompleteSqlMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea55f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea55f-113">-DefaultProfile</span></span>
<span data-ttu-id="ea55f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea55f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea55f-115">-NazwaProjektu</span><span class="sxs-lookup"><span data-stu-id="ea55f-115">-ProjectName</span></span>
<span data-ttu-id="ea55f-116">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="ea55f-116">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea55f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea55f-117">-ResourceGroupName</span></span>
<span data-ttu-id="ea55f-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea55f-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea55f-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ea55f-119">-ServiceName</span></span>
<span data-ttu-id="ea55f-120">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ea55f-120">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea55f-121">-Nazwa_zadania</span><span class="sxs-lookup"><span data-stu-id="ea55f-121">-TaskName</span></span>
<span data-ttu-id="ea55f-122">Nazwa zadania, na którym jest uruchamiane polecenie.</span><span class="sxs-lookup"><span data-stu-id="ea55f-122">The name of the task the command is run on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="ea55f-123">-NazwaObiektu</span><span class="sxs-lookup"><span data-stu-id="ea55f-123">-ObjectName</span></span>
<span data-ttu-id="ea55f-124">Nazwa obiektu bazy danych, względem którego zostanie uruchomione polecenie.</span><span class="sxs-lookup"><span data-stu-id="ea55f-124">The name of the database object the command will run against.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea55f-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea55f-125">-Confirm</span></span>
<span data-ttu-id="ea55f-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea55f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea55f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea55f-127">-WhatIf</span></span>
<span data-ttu-id="ea55f-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea55f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea55f-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ea55f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea55f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea55f-130">CommonParameters</span></span>
<span data-ttu-id="ea55f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea55f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea55f-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea55f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea55f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea55f-133">INPUTS</span></span>

### <span data-ttu-id="ea55f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ea55f-134">System.String</span></span>

## <span data-ttu-id="ea55f-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea55f-135">OUTPUTS</span></span>

### <span data-ttu-id="ea55f-136">Microsoft. Azure. Management. datamigration. MODELES. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="ea55f-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="ea55f-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea55f-137">NOTES</span></span>

## <span data-ttu-id="ea55f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea55f-138">RELATED LINKS</span></span>
