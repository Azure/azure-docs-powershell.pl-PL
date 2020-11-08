---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
ms.openlocfilehash: e53857533770d6de0040d2d777020f1a2f9f320a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233893"
---
# <span data-ttu-id="ee026-101">Get-AzSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="ee026-101">Get-AzSqlServerServiceObjective</span></span>

## <span data-ttu-id="ee026-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee026-102">SYNOPSIS</span></span>
<span data-ttu-id="ee026-103">Umożliwia pobieranie celów usługi dla serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ee026-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="ee026-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee026-104">SYNTAX</span></span>

### <span data-ttu-id="ee026-105">ByLocation (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ee026-105">ByLocation (Default)</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee026-106">ByServer</span><span class="sxs-lookup"><span data-stu-id="ee026-106">ByServer</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ResourceGroupName] <String>
 [-ServerName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee026-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ee026-107">DESCRIPTION</span></span>
<span data-ttu-id="ee026-108">Polecenie cmdlet **Get-AzSqlServerServiceObjective** Pobiera dostępne cele usługi dla serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ee026-108">The **Get-AzSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="ee026-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee026-109">EXAMPLES</span></span>

### <span data-ttu-id="ee026-110">Przykład 1: uzyskiwanie celów dotyczących usługi</span><span class="sxs-lookup"><span data-stu-id="ee026-110">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="ee026-111">To polecenie uzyskuje cele usługi dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="ee026-111">This command gets the service objectives for the server named Server01.</span></span>

### <span data-ttu-id="ee026-112">Przykład 2: uzyskiwanie celów serwisowych przy użyciu funkcji filtrowania</span><span class="sxs-lookup"><span data-stu-id="ee026-112">Example 2: Get service objectives using filtering</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServiceObjectiveName "P*"
ServiceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
```

<span data-ttu-id="ee026-113">To polecenie uzyskuje cele usługi dla serwera o nazwie Server01, który rozpoczyna się od "system".</span><span class="sxs-lookup"><span data-stu-id="ee026-113">This command gets the service objectives for the server named Server01 that start with "System".</span></span>

### <span data-ttu-id="ee026-114">Przykład 3: uzyskiwanie celów usługi dla lokalizacji</span><span class="sxs-lookup"><span data-stu-id="ee026-114">Example 3: Get service objectives for a location</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -Location "west us"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="ee026-115">To polecenie umożliwia pobieranie celów usługi dla określonego regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ee026-115">This command gets the service objectives for a specified Azure region.</span></span>

## <span data-ttu-id="ee026-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee026-116">PARAMETERS</span></span>

### <span data-ttu-id="ee026-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee026-117">-DefaultProfile</span></span>
<span data-ttu-id="ee026-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ee026-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee026-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ee026-119">-Location</span></span>
<span data-ttu-id="ee026-120">Nazwa lokalizacji, w której mają zostać wyświetlone cele usługi.</span><span class="sxs-lookup"><span data-stu-id="ee026-120">The name of the Location for which to get the service objectives.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee026-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee026-121">-ResourceGroupName</span></span>
<span data-ttu-id="ee026-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ee026-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ee026-123">To polecenie cmdlet umożliwia pobieranie celów usługi dla serwera bazy danych SQL przypisanego do tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="ee026-123">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee026-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ee026-124">-ServerName</span></span>
<span data-ttu-id="ee026-125">Określa nazwę serwera bazy danych SQL bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="ee026-125">Specifies the name of a SQL Database SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee026-126">-Servicecelname</span><span class="sxs-lookup"><span data-stu-id="ee026-126">-ServiceObjectiveName</span></span>
<span data-ttu-id="ee026-127">Określa nazwę celu usługi dla serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ee026-127">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="ee026-128">Dopuszczalne wartości tego parametru to: Basic, S0, S1, S2, P1, P2 i P3.</span><span class="sxs-lookup"><span data-stu-id="ee026-128">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee026-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ee026-129">-Confirm</span></span>
<span data-ttu-id="ee026-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee026-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee026-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee026-131">-WhatIf</span></span>
<span data-ttu-id="ee026-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee026-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee026-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ee026-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee026-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee026-134">CommonParameters</span></span>
<span data-ttu-id="ee026-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee026-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee026-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee026-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee026-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee026-137">INPUTS</span></span>

### <span data-ttu-id="ee026-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ee026-138">System.String</span></span>

## <span data-ttu-id="ee026-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee026-139">OUTPUTS</span></span>

### <span data-ttu-id="ee026-140">Microsoft. Azure. Commands. SQL. serviceobject. model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="ee026-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="ee026-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee026-141">NOTES</span></span>

## <span data-ttu-id="ee026-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee026-142">RELATED LINKS</span></span>

[<span data-ttu-id="ee026-143">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ee026-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


