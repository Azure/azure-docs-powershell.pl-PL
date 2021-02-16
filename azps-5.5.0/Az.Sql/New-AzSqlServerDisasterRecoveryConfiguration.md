---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a294fd3db4ded19dba2ebd55547ec1c6cbfa9c68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178379"
---
# <span data-ttu-id="013eb-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="013eb-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="013eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="013eb-102">SYNOPSIS</span></span>
<span data-ttu-id="013eb-103">Tworzy konfigurację odzyskiwania systemu serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="013eb-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="013eb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="013eb-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="013eb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="013eb-105">DESCRIPTION</span></span>
<span data-ttu-id="013eb-106">Polecenie **cmdlet New-AzSqlServerDisasterRecoveryConfiguration** tworzy konfigurację odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="013eb-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="013eb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="013eb-107">EXAMPLES</span></span>

## <span data-ttu-id="013eb-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="013eb-108">PARAMETERS</span></span>

### <span data-ttu-id="013eb-109">— AsJob</span><span class="sxs-lookup"><span data-stu-id="013eb-109">-AsJob</span></span>
<span data-ttu-id="013eb-110">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="013eb-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="013eb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="013eb-111">-DefaultProfile</span></span>
<span data-ttu-id="013eb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="013eb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="013eb-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="013eb-113">-FailoverPolicy</span></span>
<span data-ttu-id="013eb-114">Określa zasady trybu failover.</span><span class="sxs-lookup"><span data-stu-id="013eb-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="013eb-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="013eb-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="013eb-116">Określa nazwę grupy zasobów partnerów.</span><span class="sxs-lookup"><span data-stu-id="013eb-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="013eb-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="013eb-117">-PartnerServerName</span></span>
<span data-ttu-id="013eb-118">Określa nazwę serwera partnerskiego.</span><span class="sxs-lookup"><span data-stu-id="013eb-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="013eb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="013eb-119">-ResourceGroupName</span></span>
<span data-ttu-id="013eb-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="013eb-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="013eb-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="013eb-121">-ServerName</span></span>
<span data-ttu-id="013eb-122">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="013eb-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="013eb-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="013eb-123">-VirtualEndpointName</span></span>
<span data-ttu-id="013eb-124">Określa nazwę wirtualnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="013eb-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="013eb-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="013eb-125">-Confirm</span></span>
<span data-ttu-id="013eb-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="013eb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="013eb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="013eb-127">-WhatIf</span></span>
<span data-ttu-id="013eb-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="013eb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="013eb-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="013eb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="013eb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="013eb-130">CommonParameters</span></span>
<span data-ttu-id="013eb-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="013eb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="013eb-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="013eb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="013eb-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="013eb-133">INPUTS</span></span>

### <span data-ttu-id="013eb-134">System.String</span><span class="sxs-lookup"><span data-stu-id="013eb-134">System.String</span></span>

## <span data-ttu-id="013eb-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="013eb-135">OUTPUTS</span></span>

### <span data-ttu-id="013eb-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="013eb-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="013eb-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="013eb-137">NOTES</span></span>

## <span data-ttu-id="013eb-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="013eb-138">RELATED LINKS</span></span>

[<span data-ttu-id="013eb-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="013eb-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="013eb-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="013eb-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="013eb-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="013eb-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="013eb-142">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="013eb-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
