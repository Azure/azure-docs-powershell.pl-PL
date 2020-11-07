---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 8f1400ba07444a5fc14d2a3194edd9fe960aaccc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707846"
---
# <span data-ttu-id="ac31e-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac31e-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="ac31e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac31e-102">SYNOPSIS</span></span>
<span data-ttu-id="ac31e-103">Umożliwia utworzenie konfiguracji odzyskiwania systemu serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ac31e-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="ac31e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac31e-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac31e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ac31e-105">DESCRIPTION</span></span>
<span data-ttu-id="ac31e-106">Polecenie cmdlet **New-AzSqlServerDisasterRecoveryConfiguration** umożliwia utworzenie konfiguracji odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="ac31e-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="ac31e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac31e-107">EXAMPLES</span></span>

## <span data-ttu-id="ac31e-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac31e-108">PARAMETERS</span></span>

### <span data-ttu-id="ac31e-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac31e-109">-AsJob</span></span>
<span data-ttu-id="ac31e-110">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ac31e-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac31e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac31e-111">-DefaultProfile</span></span>
<span data-ttu-id="ac31e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ac31e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac31e-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="ac31e-113">-FailoverPolicy</span></span>
<span data-ttu-id="ac31e-114">Określa zasady pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="ac31e-114">Specifies the failover policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac31e-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac31e-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="ac31e-116">Określa nazwę grupy zasobów partnera.</span><span class="sxs-lookup"><span data-stu-id="ac31e-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="ac31e-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="ac31e-117">-PartnerServerName</span></span>
<span data-ttu-id="ac31e-118">Określa nazwę serwera partnerskiego.</span><span class="sxs-lookup"><span data-stu-id="ac31e-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="ac31e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac31e-119">-ResourceGroupName</span></span>
<span data-ttu-id="ac31e-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ac31e-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ac31e-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ac31e-121">-ServerName</span></span>
<span data-ttu-id="ac31e-122">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="ac31e-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="ac31e-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="ac31e-123">-VirtualEndpointName</span></span>
<span data-ttu-id="ac31e-124">Określa nazwę wirtualnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="ac31e-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="ac31e-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ac31e-125">-Confirm</span></span>
<span data-ttu-id="ac31e-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac31e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac31e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac31e-127">-WhatIf</span></span>
<span data-ttu-id="ac31e-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac31e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac31e-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ac31e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac31e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac31e-130">CommonParameters</span></span>
<span data-ttu-id="ac31e-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac31e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac31e-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac31e-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac31e-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac31e-133">INPUTS</span></span>

### <span data-ttu-id="ac31e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ac31e-134">System.String</span></span>

## <span data-ttu-id="ac31e-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac31e-135">OUTPUTS</span></span>

### <span data-ttu-id="ac31e-136">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="ac31e-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="ac31e-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac31e-137">NOTES</span></span>

## <span data-ttu-id="ac31e-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac31e-138">RELATED LINKS</span></span>

[<span data-ttu-id="ac31e-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac31e-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ac31e-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac31e-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ac31e-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac31e-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ac31e-142">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ac31e-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)