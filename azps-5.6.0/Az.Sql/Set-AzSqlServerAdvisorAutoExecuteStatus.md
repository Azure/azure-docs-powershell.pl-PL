---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: a80656e0a85401c4a98b62823b2b19ec2294d2f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014481"
---
# <span data-ttu-id="50457-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="50457-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="50457-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50457-102">SYNOPSIS</span></span>
<span data-ttu-id="50457-103">Aktualizuje stan automatycznego wykonywania doradcy programu Azure SQL Server Advisor.</span><span class="sxs-lookup"><span data-stu-id="50457-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="50457-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="50457-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50457-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="50457-105">DESCRIPTION</span></span>
<span data-ttu-id="50457-106">Polecenie **cmdlet Set-AzSqlServerAdvisorAutoExecuteStatus** ustawia właściwość auto execute dla doradcy programu Azure SQL Server Advisor.</span><span class="sxs-lookup"><span data-stu-id="50457-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="50457-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="50457-107">EXAMPLES</span></span>

### <span data-ttu-id="50457-108">Przykład 1. Włączanie automatycznego wykonywania dla doradcy</span><span class="sxs-lookup"><span data-stu-id="50457-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Server
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="50457-109">To polecenie umożliwia automatyczne wykonywanie stanu doradcy o nazwie CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="50457-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="50457-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50457-110">PARAMETERS</span></span>

### <span data-ttu-id="50457-111">- AdvisorName</span><span class="sxs-lookup"><span data-stu-id="50457-111">-AdvisorName</span></span>
<span data-ttu-id="50457-112">Określa nazwę doradcy, dla którego to polecenie cmdlet aktualizuje stan autowy wykonania.</span><span class="sxs-lookup"><span data-stu-id="50457-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="50457-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="50457-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="50457-114">Określa wartość, dla której to polecenie cmdlet aktualizuje stan autowy wykonania.</span><span class="sxs-lookup"><span data-stu-id="50457-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="50457-115">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="50457-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="50457-116">Włączone</span><span class="sxs-lookup"><span data-stu-id="50457-116">Enabled</span></span>
- <span data-ttu-id="50457-117">Wyłączone</span><span class="sxs-lookup"><span data-stu-id="50457-117">Disabled</span></span>
- <span data-ttu-id="50457-118">Domyślne</span><span class="sxs-lookup"><span data-stu-id="50457-118">Default</span></span>

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

### <span data-ttu-id="50457-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50457-119">-DefaultProfile</span></span>
<span data-ttu-id="50457-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="50457-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50457-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50457-121">-ResourceGroupName</span></span>
<span data-ttu-id="50457-122">Określa nazwę grupy zasobów serwera.</span><span class="sxs-lookup"><span data-stu-id="50457-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="50457-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="50457-123">-ServerName</span></span>
<span data-ttu-id="50457-124">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="50457-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="50457-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="50457-125">-Confirm</span></span>
<span data-ttu-id="50457-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="50457-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50457-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50457-127">-WhatIf</span></span>
<span data-ttu-id="50457-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50457-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50457-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="50457-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50457-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50457-130">CommonParameters</span></span>
<span data-ttu-id="50457-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50457-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50457-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50457-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50457-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50457-133">INPUTS</span></span>

### <span data-ttu-id="50457-134">System.String</span><span class="sxs-lookup"><span data-stu-id="50457-134">System.String</span></span>

### <span data-ttu-id="50457-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="50457-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="50457-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50457-136">OUTPUTS</span></span>

### <span data-ttu-id="50457-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="50457-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="50457-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="50457-138">NOTES</span></span>
* <span data-ttu-id="50457-139">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, sql, server, mssql, doradca</span><span class="sxs-lookup"><span data-stu-id="50457-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="50457-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50457-140">RELATED LINKS</span></span>

[<span data-ttu-id="50457-141">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="50457-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="50457-142">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="50457-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
