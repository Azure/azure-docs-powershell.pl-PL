---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: e99e2e6a8c0b2c8a0fc0b2d2143d2b4301520ab0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952650"
---
# <span data-ttu-id="8542c-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="8542c-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="8542c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8542c-102">SYNOPSIS</span></span>
<span data-ttu-id="8542c-103">Tworzy nowe polecenie do wykonania dla istniejącego zadania DMS.</span><span class="sxs-lookup"><span data-stu-id="8542c-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="8542c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8542c-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="8542c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8542c-105">DESCRIPTION</span></span>
<span data-ttu-id="8542c-106">Polecenie Invoke-AzDataMigrationCommand tworzy nowe zadanie polecenia do uruchomienia dla istniejącego zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="8542c-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="8542c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8542c-107">EXAMPLES</span></span>

### <span data-ttu-id="8542c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8542c-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="8542c-109">W powyższych przykładach Invoke-AzDataMigrationCommand polecenie cmdlet w celu utworzenia polecenia dla istniejącej usługi, projektu i zadania</span><span class="sxs-lookup"><span data-stu-id="8542c-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="8542c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8542c-110">PARAMETERS</span></span>

### <span data-ttu-id="8542c-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="8542c-111">-CommandType</span></span>
<span data-ttu-id="8542c-112">Typ polecenia.</span><span class="sxs-lookup"><span data-stu-id="8542c-112">Command Type.</span></span>

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

### <span data-ttu-id="8542c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8542c-113">-DefaultProfile</span></span>
<span data-ttu-id="8542c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8542c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8542c-115">— Nazwa_projektu</span><span class="sxs-lookup"><span data-stu-id="8542c-115">-ProjectName</span></span>
<span data-ttu-id="8542c-116">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="8542c-116">The name of the project.</span></span>

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

### <span data-ttu-id="8542c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8542c-117">-ResourceGroupName</span></span>
<span data-ttu-id="8542c-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8542c-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="8542c-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8542c-119">-ServiceName</span></span>
<span data-ttu-id="8542c-120">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8542c-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="8542c-121">— Nazwa_zadania</span><span class="sxs-lookup"><span data-stu-id="8542c-121">-TaskName</span></span>
<span data-ttu-id="8542c-122">Nazwa zadania, dla których jest uruchamiane polecenie.</span><span class="sxs-lookup"><span data-stu-id="8542c-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="8542c-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="8542c-123">-ObjectName</span></span>
<span data-ttu-id="8542c-124">Nazwa obiektu bazy danych, dla których zostanie uruchomione polecenie.</span><span class="sxs-lookup"><span data-stu-id="8542c-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="8542c-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8542c-125">-Confirm</span></span>
<span data-ttu-id="8542c-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8542c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8542c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8542c-127">-WhatIf</span></span>
<span data-ttu-id="8542c-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8542c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8542c-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8542c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8542c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8542c-130">CommonParameters</span></span>
<span data-ttu-id="8542c-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8542c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8542c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8542c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8542c-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8542c-133">INPUTS</span></span>

### <span data-ttu-id="8542c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8542c-134">System.String</span></span>

## <span data-ttu-id="8542c-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8542c-135">OUTPUTS</span></span>

### <span data-ttu-id="8542c-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span><span class="sxs-lookup"><span data-stu-id="8542c-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="8542c-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8542c-137">NOTES</span></span>

## <span data-ttu-id="8542c-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8542c-138">RELATED LINKS</span></span>
