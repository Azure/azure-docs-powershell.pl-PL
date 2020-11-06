---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: f483d3deb6c4e4ee6fb5c091dffc9b7969766d6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548279"
---
# <span data-ttu-id="7731c-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="7731c-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="7731c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7731c-102">SYNOPSIS</span></span>
<span data-ttu-id="7731c-103">Aktualizuje stan automatycznego wykonywania usługi Azure SQL Server Advisor.</span><span class="sxs-lookup"><span data-stu-id="7731c-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7731c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7731c-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7731c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7731c-105">DESCRIPTION</span></span>
<span data-ttu-id="7731c-106">Polecenie cmdlet **Set-AzureRmSqlServerAdvisorAutoExecuteStatus** ustawia właściwość automatycznego wykonywania dla usługi Azure SQL Server Advisor.</span><span class="sxs-lookup"><span data-stu-id="7731c-106">The **Set-AzureRmSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="7731c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7731c-107">EXAMPLES</span></span>

### <span data-ttu-id="7731c-108">Przykład 1: Włączanie automatycznego wykonywania dla klasyfikatora</span><span class="sxs-lookup"><span data-stu-id="7731c-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzureRmSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
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

<span data-ttu-id="7731c-109">To polecenie włącza stan automatycznego wykonywania klasyfikatora o nazwie Moja indeks.</span><span class="sxs-lookup"><span data-stu-id="7731c-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="7731c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7731c-110">PARAMETERS</span></span>

### <span data-ttu-id="7731c-111">-Klasyfikatorname</span><span class="sxs-lookup"><span data-stu-id="7731c-111">-AdvisorName</span></span>
<span data-ttu-id="7731c-112">Określa nazwę klasyfikatora, dla którego to polecenie cmdlet aktualizuje stan automatycznego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="7731c-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="7731c-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="7731c-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="7731c-114">Określa wartość, na którą to polecenie cmdlet aktualizuje stan automatycznego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="7731c-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="7731c-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7731c-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7731c-116">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="7731c-116">Enabled</span></span>
- <span data-ttu-id="7731c-117">Łącza</span><span class="sxs-lookup"><span data-stu-id="7731c-117">Disabled</span></span>
- <span data-ttu-id="7731c-118">Domyślne</span><span class="sxs-lookup"><span data-stu-id="7731c-118">Default</span></span>

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

### <span data-ttu-id="7731c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7731c-119">-ResourceGroupName</span></span>
<span data-ttu-id="7731c-120">Określa nazwę grupy zasobów serwera.</span><span class="sxs-lookup"><span data-stu-id="7731c-120">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="7731c-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="7731c-121">-ServerName</span></span>
<span data-ttu-id="7731c-122">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="7731c-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="7731c-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7731c-123">-Confirm</span></span>
<span data-ttu-id="7731c-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7731c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7731c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7731c-125">-WhatIf</span></span>
<span data-ttu-id="7731c-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7731c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7731c-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7731c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7731c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7731c-128">-DefaultProfile</span></span>
<span data-ttu-id="7731c-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7731c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7731c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7731c-130">CommonParameters</span></span>
<span data-ttu-id="7731c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7731c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7731c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7731c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7731c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7731c-133">INPUTS</span></span>

## <span data-ttu-id="7731c-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7731c-134">OUTPUTS</span></span>

### <span data-ttu-id="7731c-135">Microsoft. Azure. Commands. SQL. Advisor. model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="7731c-135">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="7731c-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7731c-136">NOTES</span></span>
* <span data-ttu-id="7731c-137">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Server, MSSQL, Doradca</span><span class="sxs-lookup"><span data-stu-id="7731c-137">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="7731c-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7731c-138">RELATED LINKS</span></span>

[<span data-ttu-id="7731c-139">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="7731c-139">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="7731c-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="7731c-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
