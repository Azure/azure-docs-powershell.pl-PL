---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Invoke-AzureRmDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
ms.openlocfilehash: 882d7eb0b005478850addda2d066c7266e6c2ad0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548695"
---
# <span data-ttu-id="6ded4-101">Invoke-AzureRmDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="6ded4-101">Invoke-AzureRmDataMigrationCommand</span></span>

## <span data-ttu-id="6ded4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ded4-102">SYNOPSIS</span></span>
<span data-ttu-id="6ded4-103">Tworzy nowe polecenie do wykonania na istniejącym zadaniu DMS.</span><span class="sxs-lookup"><span data-stu-id="6ded4-103">Creates a new command to be executed on an existing DMS task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ded4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ded4-104">SYNTAX</span></span>

```
Invoke-AzureRmDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ded4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6ded4-105">DESCRIPTION</span></span>
<span data-ttu-id="6ded4-106">Polecenie cmdlet New-AzureRmDataMigrationCommand tworzy nowe zadanie w celu uruchomienia go w istniejącym zadaniu migracji.</span><span class="sxs-lookup"><span data-stu-id="6ded4-106">The New-AzureRmDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="6ded4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ded4-107">EXAMPLES</span></span>

### <span data-ttu-id="6ded4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6ded4-108">Example 1</span></span>
```
PS C:\> $command = New-AzureRmDmsCommand -CommandType Complete -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="6ded4-109">W powyższych przykładach użyto polecenia cmdlet New-AzureRmDmsCommand, aby utworzyć polecenie dla istniejącej usługi, projektu i zadania.</span><span class="sxs-lookup"><span data-stu-id="6ded4-109">The above examples uses the New-AzureRmDmsCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="6ded4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ded4-110">PARAMETERS</span></span>

### <span data-ttu-id="6ded4-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="6ded4-111">-CommandType</span></span>
<span data-ttu-id="6ded4-112">Typ polecenia.</span><span class="sxs-lookup"><span data-stu-id="6ded4-112">Command Type.</span></span>

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

### <span data-ttu-id="6ded4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ded4-113">-DefaultProfile</span></span>
<span data-ttu-id="6ded4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ded4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ded4-115">-NazwaProjektu</span><span class="sxs-lookup"><span data-stu-id="6ded4-115">-ProjectName</span></span>
<span data-ttu-id="6ded4-116">Nazwa projektu.</span><span class="sxs-lookup"><span data-stu-id="6ded4-116">The name of the project.</span></span>

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

### <span data-ttu-id="6ded4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ded4-117">-ResourceGroupName</span></span>
<span data-ttu-id="6ded4-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6ded4-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="6ded4-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6ded4-119">-ServiceName</span></span>
<span data-ttu-id="6ded4-120">Nazwa usługi migracji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6ded4-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="6ded4-121">-Nazwa_zadania</span><span class="sxs-lookup"><span data-stu-id="6ded4-121">-TaskName</span></span>
<span data-ttu-id="6ded4-122">Nazwa zadania, na którym jest uruchamiane polecenie.</span><span class="sxs-lookup"><span data-stu-id="6ded4-122">The name of the task the command is run on.</span></span>

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

### <span data-ttu-id="6ded4-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ded4-123">-Confirm</span></span>
<span data-ttu-id="6ded4-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ded4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ded4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ded4-125">-WhatIf</span></span>
<span data-ttu-id="6ded4-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ded4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ded4-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ded4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ded4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ded4-128">CommonParameters</span></span>
<span data-ttu-id="6ded4-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ded4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ded4-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ded4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ded4-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ded4-131">INPUTS</span></span>

### <span data-ttu-id="6ded4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6ded4-132">System.String</span></span>

## <span data-ttu-id="6ded4-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ded4-133">OUTPUTS</span></span>

### <span data-ttu-id="6ded4-134">Microsoft. Azure. Management. datamigration. MODELES. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="6ded4-134">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="6ded4-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ded4-135">NOTES</span></span>

## <span data-ttu-id="6ded4-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ded4-136">RELATED LINKS</span></span>
