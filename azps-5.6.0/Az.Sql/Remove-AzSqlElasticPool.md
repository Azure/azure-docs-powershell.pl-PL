---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: 565d22bc2860acc69f5d919bf000a564d9295ce5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955162"
---
# <span data-ttu-id="6009d-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6009d-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="6009d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6009d-102">SYNOPSIS</span></span>
<span data-ttu-id="6009d-103">Usuwa elastyczną pulę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6009d-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="6009d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6009d-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6009d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6009d-105">DESCRIPTION</span></span>
<span data-ttu-id="6009d-106">Polecenie **cmdlet Remove-AzSqlElasticPool** usuwa pulę elastyczną usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="6009d-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="6009d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6009d-107">EXAMPLES</span></span>

### <span data-ttu-id="6009d-108">Przykład 1. Usuwanie puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="6009d-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="6009d-109">To polecenie usuwa elastyczną pulę o nazwiePoolpool01.</span><span class="sxs-lookup"><span data-stu-id="6009d-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="6009d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6009d-110">PARAMETERS</span></span>

### <span data-ttu-id="6009d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6009d-111">-DefaultProfile</span></span>
<span data-ttu-id="6009d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6009d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6009d-113">-Nawiązywane_buforyNazwa</span><span class="sxs-lookup"><span data-stu-id="6009d-113">-ElasticPoolName</span></span>
<span data-ttu-id="6009d-114">Określa nazwę elastycznej puli usuwaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6009d-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6009d-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6009d-115">-Force</span></span>
<span data-ttu-id="6009d-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6009d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6009d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6009d-117">-ResourceGroupName</span></span>
<span data-ttu-id="6009d-118">Określa nazwę grupy zasobów, do której jest przypisana pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="6009d-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="6009d-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6009d-119">-ServerName</span></span>
<span data-ttu-id="6009d-120">Określa nazwę serwera hostowego elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="6009d-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="6009d-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6009d-121">-Confirm</span></span>
<span data-ttu-id="6009d-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6009d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6009d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6009d-123">-WhatIf</span></span>
<span data-ttu-id="6009d-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6009d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6009d-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6009d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6009d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6009d-126">CommonParameters</span></span>
<span data-ttu-id="6009d-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6009d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6009d-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6009d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6009d-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6009d-129">INPUTS</span></span>

### <span data-ttu-id="6009d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6009d-130">System.String</span></span>

## <span data-ttu-id="6009d-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6009d-131">OUTPUTS</span></span>

### <span data-ttu-id="6009d-132">Microsoft.Azure.Commands.Sql.NawiązywekPoola.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="6009d-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="6009d-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6009d-133">NOTES</span></span>

## <span data-ttu-id="6009d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6009d-134">RELATED LINKS</span></span>

[<span data-ttu-id="6009d-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6009d-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="6009d-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="6009d-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="6009d-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="6009d-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="6009d-138">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6009d-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="6009d-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6009d-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="6009d-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="6009d-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


