---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: aa3aff9a1e471445c49cbfb23b5799a97c54025d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887217"
---
# <span data-ttu-id="4e612-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="4e612-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="4e612-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e612-102">SYNOPSIS</span></span>
<span data-ttu-id="4e612-103">Aktualizuje stan automatycznego wykonywania usługi Azure SQL Server Advisor.</span><span class="sxs-lookup"><span data-stu-id="4e612-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="4e612-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e612-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e612-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4e612-105">DESCRIPTION</span></span>
<span data-ttu-id="4e612-106">Polecenie cmdlet **Set-AzSqlServerAdvisorAutoExecuteStatus** ustawia właściwość automatycznego wykonywania dla usługi Azure SQL Server Advisor.</span><span class="sxs-lookup"><span data-stu-id="4e612-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="4e612-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e612-107">EXAMPLES</span></span>

### <span data-ttu-id="4e612-108">Przykład 1: Włączanie automatycznego wykonywania dla klasyfikatora</span><span class="sxs-lookup"><span data-stu-id="4e612-108">Example 1: Enable auto execute for an Advisor</span></span>
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

<span data-ttu-id="4e612-109">To polecenie włącza stan automatycznego wykonywania klasyfikatora o nazwie Moja indeks.</span><span class="sxs-lookup"><span data-stu-id="4e612-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="4e612-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e612-110">PARAMETERS</span></span>

### <span data-ttu-id="4e612-111">-Klasyfikatorname</span><span class="sxs-lookup"><span data-stu-id="4e612-111">-AdvisorName</span></span>
<span data-ttu-id="4e612-112">Określa nazwę klasyfikatora, dla którego to polecenie cmdlet aktualizuje stan automatycznego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="4e612-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="4e612-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="4e612-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="4e612-114">Określa wartość, na którą to polecenie cmdlet aktualizuje stan automatycznego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="4e612-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="4e612-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4e612-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e612-116">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="4e612-116">Enabled</span></span>
- <span data-ttu-id="4e612-117">Łącza</span><span class="sxs-lookup"><span data-stu-id="4e612-117">Disabled</span></span>
- <span data-ttu-id="4e612-118">Domyślne</span><span class="sxs-lookup"><span data-stu-id="4e612-118">Default</span></span>

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

### <span data-ttu-id="4e612-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e612-119">-DefaultProfile</span></span>
<span data-ttu-id="4e612-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4e612-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e612-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e612-121">-ResourceGroupName</span></span>
<span data-ttu-id="4e612-122">Określa nazwę grupy zasobów serwera.</span><span class="sxs-lookup"><span data-stu-id="4e612-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="4e612-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4e612-123">-ServerName</span></span>
<span data-ttu-id="4e612-124">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="4e612-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="4e612-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4e612-125">-Confirm</span></span>
<span data-ttu-id="4e612-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e612-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e612-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e612-127">-WhatIf</span></span>
<span data-ttu-id="4e612-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e612-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e612-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4e612-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e612-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e612-130">CommonParameters</span></span>
<span data-ttu-id="4e612-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e612-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e612-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e612-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e612-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e612-133">INPUTS</span></span>

### <span data-ttu-id="4e612-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4e612-134">System.String</span></span>

### <span data-ttu-id="4e612-135">Microsoft. Azure. Commands. SQL. Advisor. cmdlet. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="4e612-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="4e612-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e612-136">OUTPUTS</span></span>

### <span data-ttu-id="4e612-137">Microsoft. Azure. Commands. SQL. Advisor. model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="4e612-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="4e612-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e612-138">NOTES</span></span>
* <span data-ttu-id="4e612-139">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Server, MSSQL, Doradca</span><span class="sxs-lookup"><span data-stu-id="4e612-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="4e612-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e612-140">RELATED LINKS</span></span>

[<span data-ttu-id="4e612-141">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="4e612-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="4e612-142">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="4e612-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
