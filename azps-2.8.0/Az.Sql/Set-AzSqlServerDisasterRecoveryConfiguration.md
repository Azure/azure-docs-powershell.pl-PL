---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: b3a84fc37e747cb54571bc26563789599fac3a7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887105"
---
# <span data-ttu-id="58d3a-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="58d3a-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="58d3a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58d3a-102">SYNOPSIS</span></span>
<span data-ttu-id="58d3a-103">Modyfikuje konfigurację odzyskiwania serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="58d3a-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="58d3a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58d3a-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58d3a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58d3a-105">DESCRIPTION</span></span>
<span data-ttu-id="58d3a-106">Polecenie cmdlet **Set-AzSqlServerDisasterRecoveryConfiguration** modyfikuje konfigurację odzyskiwania serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="58d3a-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="58d3a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58d3a-107">EXAMPLES</span></span>

## <span data-ttu-id="58d3a-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58d3a-108">PARAMETERS</span></span>

### <span data-ttu-id="58d3a-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="58d3a-109">-AllowDataLoss</span></span>
<span data-ttu-id="58d3a-110">Wskazuje, że operacja przełączania awaryjnego umożliwia utratę danych.</span><span class="sxs-lookup"><span data-stu-id="58d3a-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="58d3a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58d3a-111">-AsJob</span></span>
<span data-ttu-id="58d3a-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="58d3a-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58d3a-113">-DefaultProfile</span></span>
<span data-ttu-id="58d3a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="58d3a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58d3a-115">-Praca awaryjna</span><span class="sxs-lookup"><span data-stu-id="58d3a-115">-Failover</span></span>
<span data-ttu-id="58d3a-116">Wskazuje, że ta operacja jest przejściem do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="58d3a-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d3a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58d3a-117">-ResourceGroupName</span></span>
<span data-ttu-id="58d3a-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="58d3a-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="58d3a-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="58d3a-119">-ServerName</span></span>
<span data-ttu-id="58d3a-120">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="58d3a-120">Specifies the name of a SQL database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58d3a-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="58d3a-121">-VirtualEndpointName</span></span>
<span data-ttu-id="58d3a-122">Określa nazwę wirtualnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="58d3a-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="58d3a-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58d3a-123">-Confirm</span></span>
<span data-ttu-id="58d3a-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58d3a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58d3a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58d3a-125">-WhatIf</span></span>
<span data-ttu-id="58d3a-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58d3a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58d3a-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="58d3a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58d3a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d3a-128">CommonParameters</span></span>
<span data-ttu-id="58d3a-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58d3a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d3a-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58d3a-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d3a-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58d3a-131">INPUTS</span></span>

### <span data-ttu-id="58d3a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="58d3a-132">System.String</span></span>

## <span data-ttu-id="58d3a-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58d3a-133">OUTPUTS</span></span>

### <span data-ttu-id="58d3a-134">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="58d3a-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="58d3a-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58d3a-135">NOTES</span></span>

## <span data-ttu-id="58d3a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58d3a-136">RELATED LINKS</span></span>

[<span data-ttu-id="58d3a-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="58d3a-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="58d3a-138">Nowe — AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="58d3a-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="58d3a-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="58d3a-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="58d3a-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="58d3a-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
