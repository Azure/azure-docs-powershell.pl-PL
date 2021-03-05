---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 10da2a625eb3858e77343275246d8a142fefc504
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995170"
---
# <span data-ttu-id="ba471-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba471-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="ba471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba471-102">SYNOPSIS</span></span>
<span data-ttu-id="ba471-103">Usuwa konfigurację odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="ba471-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="ba471-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ba471-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba471-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ba471-105">DESCRIPTION</span></span>
<span data-ttu-id="ba471-106">Polecenie **cmdlet Remove-AzSqlServerDisasterRecoveryConfiguration** usuwa konfigurację odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="ba471-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="ba471-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ba471-107">EXAMPLES</span></span>

## <span data-ttu-id="ba471-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba471-108">PARAMETERS</span></span>

### <span data-ttu-id="ba471-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba471-109">-DefaultProfile</span></span>
<span data-ttu-id="ba471-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ba471-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba471-111">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ba471-111">-Force</span></span>
<span data-ttu-id="ba471-112">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ba471-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ba471-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba471-113">-ResourceGroupName</span></span>
<span data-ttu-id="ba471-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ba471-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ba471-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ba471-115">-ServerName</span></span>
<span data-ttu-id="ba471-116">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="ba471-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="ba471-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="ba471-117">-VirtualEndpointName</span></span>
<span data-ttu-id="ba471-118">Określa nazwę wirtualnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="ba471-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba471-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ba471-119">-Confirm</span></span>
<span data-ttu-id="ba471-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ba471-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba471-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba471-121">-WhatIf</span></span>
<span data-ttu-id="ba471-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba471-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba471-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ba471-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba471-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba471-124">CommonParameters</span></span>
<span data-ttu-id="ba471-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba471-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba471-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba471-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba471-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba471-127">INPUTS</span></span>

### <span data-ttu-id="ba471-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ba471-128">System.String</span></span>

## <span data-ttu-id="ba471-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba471-129">OUTPUTS</span></span>

### <span data-ttu-id="ba471-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="ba471-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="ba471-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ba471-131">NOTES</span></span>

## <span data-ttu-id="ba471-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba471-132">RELATED LINKS</span></span>

[<span data-ttu-id="ba471-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba471-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ba471-134">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba471-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ba471-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba471-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ba471-136">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ba471-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
