---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 013a7c40a5acfb4306d53e0ff5b8da1b54f86e46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999562"
---
# <span data-ttu-id="2a223-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="2a223-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="2a223-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a223-102">SYNOPSIS</span></span>
<span data-ttu-id="2a223-103">Pobiera stan operacji na elastycznej puli.</span><span class="sxs-lookup"><span data-stu-id="2a223-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="2a223-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2a223-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a223-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2a223-105">DESCRIPTION</span></span>
<span data-ttu-id="2a223-106">Polecenie **cmdlet Get-AzSqlElasticPoolActivity** pobiera stan operacji na elastycznej puli dla bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="2a223-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="2a223-107">Możesz sprawdzić stan tworzenia puli i aktualizacji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="2a223-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="2a223-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2a223-108">EXAMPLES</span></span>

### <span data-ttu-id="2a223-109">Przykład 1. Uzyskiwanie stanu operacji na elastycznej puli</span><span class="sxs-lookup"><span data-stu-id="2a223-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="2a223-110">To polecenie otrzymuje stan operacji puli elastycznej o nazwie 100000000000000000000000000000000000000000000</span><span class="sxs-lookup"><span data-stu-id="2a223-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="2a223-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a223-111">PARAMETERS</span></span>

### <span data-ttu-id="2a223-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a223-112">-DefaultProfile</span></span>
<span data-ttu-id="2a223-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="2a223-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a223-114">-Nawiązywane_buforyNazwa</span><span class="sxs-lookup"><span data-stu-id="2a223-114">-ElasticPoolName</span></span>
<span data-ttu-id="2a223-115">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="2a223-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="2a223-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="2a223-116">-OperationId</span></span>
<span data-ttu-id="2a223-117">Identyfikator operacji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="2a223-117">The ID of the operation to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a223-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a223-118">-ResourceGroupName</span></span>
<span data-ttu-id="2a223-119">Określa nazwę grupy zasobów, do której przypisano pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="2a223-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="2a223-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2a223-120">-ServerName</span></span>
<span data-ttu-id="2a223-121">Określa nazwę serwera zawierającego elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="2a223-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="2a223-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a223-122">-Confirm</span></span>
<span data-ttu-id="2a223-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2a223-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a223-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a223-124">-WhatIf</span></span>
<span data-ttu-id="2a223-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a223-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a223-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2a223-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a223-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a223-127">CommonParameters</span></span>
<span data-ttu-id="2a223-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a223-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a223-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a223-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a223-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a223-130">INPUTS</span></span>

### <span data-ttu-id="2a223-131">System.String</span><span class="sxs-lookup"><span data-stu-id="2a223-131">System.String</span></span>

### <span data-ttu-id="2a223-132">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2a223-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2a223-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a223-133">OUTPUTS</span></span>

### <span data-ttu-id="2a223-134">Microsoft.Azure.Commands.Sql.NawiązkaDkiPooli.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="2a223-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="2a223-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2a223-135">NOTES</span></span>

## <span data-ttu-id="2a223-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a223-136">RELATED LINKS</span></span>

[<span data-ttu-id="2a223-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2a223-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="2a223-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="2a223-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="2a223-139">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2a223-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="2a223-140">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2a223-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="2a223-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2a223-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


