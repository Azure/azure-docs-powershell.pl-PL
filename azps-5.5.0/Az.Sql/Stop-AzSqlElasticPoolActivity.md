---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
ms.openlocfilehash: dc1dffd84a95bd9cffac1dbafb5183d56e0b7c52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241922"
---
# <span data-ttu-id="5d457-101">Stop-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="5d457-101">Stop-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="5d457-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d457-102">SYNOPSIS</span></span>
<span data-ttu-id="5d457-103">Anuluje asynchroniczną operację aktualizacji na elastycznej puli.</span><span class="sxs-lookup"><span data-stu-id="5d457-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="5d457-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5d457-104">SYNTAX</span></span>

```
Stop-AzSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d457-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5d457-105">DESCRIPTION</span></span>
<span data-ttu-id="5d457-106">Polecenie **cmdlet Stop-AzSqlElasticPoolActivity** anuluje asynchroniczną operację aktualizacji na puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="5d457-106">The **Stop-AzSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="5d457-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5d457-107">EXAMPLES</span></span>

### <span data-ttu-id="5d457-108">Przykład 1. Anulowanie asynchronicznej operacji aktualizacji na puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="5d457-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : ElasticPool01
State           : CANCELLED
Operation       : UpdateLogicalElasticPool
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete :
```

<span data-ttu-id="5d457-109">To polecenie anuluje asynchroniczne operacje aktualizacji na puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="5d457-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="5d457-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d457-110">PARAMETERS</span></span>

### <span data-ttu-id="5d457-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d457-111">-DefaultProfile</span></span>
<span data-ttu-id="5d457-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d457-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d457-113">-PochylićPoolName</span><span class="sxs-lookup"><span data-stu-id="5d457-113">-ElasticPoolName</span></span>
<span data-ttu-id="5d457-114">Nazwa puli elastycznej sql azure.</span><span class="sxs-lookup"><span data-stu-id="5d457-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="5d457-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5d457-115">-OperationId</span></span>
<span data-ttu-id="5d457-116">Identyfikator operacji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="5d457-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="5d457-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d457-117">-PassThru</span></span>
<span data-ttu-id="5d457-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5d457-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5d457-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d457-119">-ResourceGroupName</span></span>
<span data-ttu-id="5d457-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5d457-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="5d457-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5d457-121">-ServerName</span></span>
<span data-ttu-id="5d457-122">Nazwa puli elastycznej programu Azure SQL Server, w którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="5d457-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="5d457-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d457-123">-Confirm</span></span>
<span data-ttu-id="5d457-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5d457-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d457-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d457-125">-WhatIf</span></span>
<span data-ttu-id="5d457-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d457-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d457-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5d457-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d457-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d457-128">CommonParameters</span></span>
<span data-ttu-id="5d457-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d457-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d457-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d457-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d457-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d457-131">INPUTS</span></span>

### <span data-ttu-id="5d457-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5d457-132">System.String</span></span>

### <span data-ttu-id="5d457-133">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5d457-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5d457-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d457-134">OUTPUTS</span></span>

### <span data-ttu-id="5d457-135">Microsoft.Azure.Commands.Sql.NawiązkaDkiPooli.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="5d457-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="5d457-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5d457-136">NOTES</span></span>

## <span data-ttu-id="5d457-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d457-137">RELATED LINKS</span></span>
