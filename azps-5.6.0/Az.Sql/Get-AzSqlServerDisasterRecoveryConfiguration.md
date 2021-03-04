---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: ad00759bb2babb85c17ab9efe2d7e47025434607
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982033"
---
# <span data-ttu-id="464fb-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="464fb-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="464fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="464fb-102">SYNOPSIS</span></span>
<span data-ttu-id="464fb-103">Pobiera konfigurację odzyskiwania systemu serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="464fb-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="464fb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="464fb-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="464fb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="464fb-105">DESCRIPTION</span></span>
<span data-ttu-id="464fb-106">Polecenie **cmdlet Get-AzSqlServerDisasterRecoveryConfiguration** pobiera konfigurację odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="464fb-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="464fb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="464fb-107">EXAMPLES</span></span>

## <span data-ttu-id="464fb-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="464fb-108">PARAMETERS</span></span>

### <span data-ttu-id="464fb-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="464fb-109">-DefaultProfile</span></span>
<span data-ttu-id="464fb-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="464fb-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="464fb-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="464fb-111">-ResourceGroupName</span></span>
<span data-ttu-id="464fb-112">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="464fb-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="464fb-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="464fb-113">-ServerName</span></span>
<span data-ttu-id="464fb-114">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="464fb-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="464fb-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="464fb-115">-VirtualEndpointName</span></span>
<span data-ttu-id="464fb-116">Określa nazwę wirtualnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="464fb-116">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="464fb-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="464fb-117">-Confirm</span></span>
<span data-ttu-id="464fb-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="464fb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="464fb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="464fb-119">-WhatIf</span></span>
<span data-ttu-id="464fb-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="464fb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="464fb-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="464fb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="464fb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="464fb-122">CommonParameters</span></span>
<span data-ttu-id="464fb-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="464fb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="464fb-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="464fb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="464fb-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="464fb-125">INPUTS</span></span>

### <span data-ttu-id="464fb-126">System.String</span><span class="sxs-lookup"><span data-stu-id="464fb-126">System.String</span></span>

## <span data-ttu-id="464fb-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="464fb-127">OUTPUTS</span></span>

### <span data-ttu-id="464fb-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="464fb-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="464fb-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="464fb-129">NOTES</span></span>

## <span data-ttu-id="464fb-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="464fb-130">RELATED LINKS</span></span>

[<span data-ttu-id="464fb-131">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="464fb-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="464fb-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="464fb-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="464fb-133">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="464fb-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="464fb-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="464fb-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

