---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 1d6348c5ede63dee1f76059277c8f7d142a2c327
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233273"
---
# <span data-ttu-id="b8179-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b8179-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="b8179-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8179-102">SYNOPSIS</span></span>
<span data-ttu-id="b8179-103">Modyfikuje stan automatycznego wykonywania klasyfikatora usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="b8179-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="b8179-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8179-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8179-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b8179-105">DESCRIPTION</span></span>
<span data-ttu-id="b8179-106">Polecenie cmdlet **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** modyfikuje Właściwość automatycznego wykonywania dla klasyfikatora bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="b8179-106">The **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="b8179-107">Obecnie to polecenie cmdlet obsługuje wartości włączone, wyłączone i domyślne.</span><span class="sxs-lookup"><span data-stu-id="b8179-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="b8179-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8179-108">EXAMPLES</span></span>

### <span data-ttu-id="b8179-109">Przykład 1: Włączanie automatycznego wykonywania dla klasyfikatora</span><span class="sxs-lookup"><span data-stu-id="b8179-109">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="b8179-110">To polecenie zmienia stan automatycznego wykonania klasyfikatora o nazwie "Moja indeks" na włączony.</span><span class="sxs-lookup"><span data-stu-id="b8179-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="b8179-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8179-111">PARAMETERS</span></span>

### <span data-ttu-id="b8179-112">-Klasyfikatorname</span><span class="sxs-lookup"><span data-stu-id="b8179-112">-AdvisorName</span></span>
<span data-ttu-id="b8179-113">Określa nazwę klasyfikatora, dla którego to polecenie cmdlet modyfikuje stan.</span><span class="sxs-lookup"><span data-stu-id="b8179-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="b8179-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b8179-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="b8179-115">Określa wartość stanu.</span><span class="sxs-lookup"><span data-stu-id="b8179-115">Specifies the value for the status.</span></span>
<span data-ttu-id="b8179-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b8179-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b8179-117">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="b8179-117">Enabled</span></span> 
- <span data-ttu-id="b8179-118">Łącza</span><span class="sxs-lookup"><span data-stu-id="b8179-118">Disabled</span></span> 
- <span data-ttu-id="b8179-119">Domyślne</span><span class="sxs-lookup"><span data-stu-id="b8179-119">Default</span></span>

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

### <span data-ttu-id="b8179-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b8179-120">-DatabaseName</span></span>
<span data-ttu-id="b8179-121">Określa nazwę bazy danych, dla której to polecenie cmdlet modyfikuje stan.</span><span class="sxs-lookup"><span data-stu-id="b8179-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="b8179-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8179-122">-DefaultProfile</span></span>
<span data-ttu-id="b8179-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b8179-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8179-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8179-124">-ResourceGroupName</span></span>
<span data-ttu-id="b8179-125">Określa nazwę grupy zasobów serwera, która zawiera tę bazę danych.</span><span class="sxs-lookup"><span data-stu-id="b8179-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="b8179-126">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b8179-126">-ServerName</span></span>
<span data-ttu-id="b8179-127">Określa nazwę serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b8179-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="b8179-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8179-128">-Confirm</span></span>
<span data-ttu-id="b8179-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8179-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8179-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8179-130">-WhatIf</span></span>
<span data-ttu-id="b8179-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8179-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8179-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b8179-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8179-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8179-133">CommonParameters</span></span>
<span data-ttu-id="b8179-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8179-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8179-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8179-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8179-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8179-136">INPUTS</span></span>

### <span data-ttu-id="b8179-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b8179-137">System.String</span></span>

### <span data-ttu-id="b8179-138">Microsoft. Azure. Commands. SQL. Advisor. cmdlet. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b8179-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="b8179-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8179-139">OUTPUTS</span></span>

### <span data-ttu-id="b8179-140">Microsoft. Azure. Commands. SQL. Advisor. model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="b8179-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="b8179-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8179-141">NOTES</span></span>

## <span data-ttu-id="b8179-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8179-142">RELATED LINKS</span></span>

[<span data-ttu-id="b8179-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="b8179-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="b8179-144">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b8179-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

