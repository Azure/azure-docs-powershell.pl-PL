---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 1d6348c5ede63dee1f76059277c8f7d142a2c327
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191002"
---
# <span data-ttu-id="e5fff-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="e5fff-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="e5fff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5fff-102">SYNOPSIS</span></span>
<span data-ttu-id="e5fff-103">Modyfikuje stan automatycznego wykonywania doradcy usługi Azure SQL Database Advisor.</span><span class="sxs-lookup"><span data-stu-id="e5fff-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="e5fff-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e5fff-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5fff-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e5fff-105">DESCRIPTION</span></span>
<span data-ttu-id="e5fff-106">Polecenie cmdlet **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** modyfikuje właściwość auto execute doradcy usługi Azure SQL Database Advisor.</span><span class="sxs-lookup"><span data-stu-id="e5fff-106">The **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="e5fff-107">Obecnie to polecenie cmdlet obsługuje wartości Włączone, Wyłączone i Domyślne.</span><span class="sxs-lookup"><span data-stu-id="e5fff-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="e5fff-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e5fff-108">EXAMPLES</span></span>

### <span data-ttu-id="e5fff-109">Przykład 1. Włączanie automatycznego wykonywania dla doradcy</span><span class="sxs-lookup"><span data-stu-id="e5fff-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
DatabaseName                   : ContosoRunner
ResourceGroupName              : ContosoRunnersProd
ServerName                     : runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="e5fff-110">To polecenie zmienia stan automatycznego wykonywania doradcy o nazwie CreateIndex na Włączony.</span><span class="sxs-lookup"><span data-stu-id="e5fff-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="e5fff-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5fff-111">PARAMETERS</span></span>

### <span data-ttu-id="e5fff-112">- AdvisorName</span><span class="sxs-lookup"><span data-stu-id="e5fff-112">-AdvisorName</span></span>
<span data-ttu-id="e5fff-113">Określa nazwę doradcy, dla którego to polecenie cmdlet modyfikuje stan.</span><span class="sxs-lookup"><span data-stu-id="e5fff-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="e5fff-114">- AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="e5fff-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="e5fff-115">Określa wartość stanu.</span><span class="sxs-lookup"><span data-stu-id="e5fff-115">Specifies the value for the status.</span></span>
<span data-ttu-id="e5fff-116">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e5fff-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e5fff-117">Włączone</span><span class="sxs-lookup"><span data-stu-id="e5fff-117">Enabled</span></span> 
- <span data-ttu-id="e5fff-118">Wyłączone</span><span class="sxs-lookup"><span data-stu-id="e5fff-118">Disabled</span></span> 
- <span data-ttu-id="e5fff-119">Domyślne</span><span class="sxs-lookup"><span data-stu-id="e5fff-119">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fff-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e5fff-120">-DatabaseName</span></span>
<span data-ttu-id="e5fff-121">Określa nazwę bazy danych, dla której to polecenie cmdlet modyfikuje stan.</span><span class="sxs-lookup"><span data-stu-id="e5fff-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="e5fff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5fff-122">-DefaultProfile</span></span>
<span data-ttu-id="e5fff-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e5fff-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5fff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5fff-124">-ResourceGroupName</span></span>
<span data-ttu-id="e5fff-125">Określa nazwę grupy zasobów serwera zawierającego tę bazę danych.</span><span class="sxs-lookup"><span data-stu-id="e5fff-125">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fff-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e5fff-126">-ServerName</span></span>
<span data-ttu-id="e5fff-127">Określa nazwę serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e5fff-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="e5fff-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e5fff-128">-Confirm</span></span>
<span data-ttu-id="e5fff-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e5fff-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5fff-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5fff-130">-WhatIf</span></span>
<span data-ttu-id="e5fff-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5fff-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5fff-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e5fff-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5fff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5fff-133">CommonParameters</span></span>
<span data-ttu-id="e5fff-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5fff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5fff-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5fff-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5fff-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5fff-136">INPUTS</span></span>

### <span data-ttu-id="e5fff-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e5fff-137">System.String</span></span>

### <span data-ttu-id="e5fff-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="e5fff-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="e5fff-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5fff-139">OUTPUTS</span></span>

### <span data-ttu-id="e5fff-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="e5fff-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="e5fff-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e5fff-141">NOTES</span></span>

## <span data-ttu-id="e5fff-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5fff-142">RELATED LINKS</span></span>

[<span data-ttu-id="e5fff-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="e5fff-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="e5fff-144">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="e5fff-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

