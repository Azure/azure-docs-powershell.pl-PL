---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 0082918e09c0f42910ead42d03319577d4b4c9c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707697"
---
# <span data-ttu-id="537df-101">Stop-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="537df-101">Stop-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="537df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="537df-102">SYNOPSIS</span></span>
<span data-ttu-id="537df-103">Anuluje operację aktualizacji asynchronicznej w puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="537df-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="537df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="537df-104">SYNTAX</span></span>

```
Stop-AzSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="537df-105">Opis</span><span class="sxs-lookup"><span data-stu-id="537df-105">DESCRIPTION</span></span>
<span data-ttu-id="537df-106">Polecenie cmdlet **stop-AzSqlElasticPoolActivity** anuluje operację aktualizacji asynchronicznej w puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="537df-106">The **Stop-AzSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="537df-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="537df-107">EXAMPLES</span></span>

### <span data-ttu-id="537df-108">Przykład 1. Anuluj operację aktualizacji asynchronicznej w puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="537df-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
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

<span data-ttu-id="537df-109">To polecenie anuluje operację aktualizacji asynchronicznych na puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="537df-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="537df-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="537df-110">PARAMETERS</span></span>

### <span data-ttu-id="537df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="537df-111">-DefaultProfile</span></span>
<span data-ttu-id="537df-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="537df-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="537df-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="537df-113">-ElasticPoolName</span></span>
<span data-ttu-id="537df-114">Nazwa puli elastycznej SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="537df-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="537df-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="537df-115">-OperationId</span></span>
<span data-ttu-id="537df-116">Identyfikator operacji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="537df-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="537df-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="537df-117">-PassThru</span></span>
<span data-ttu-id="537df-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="537df-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="537df-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="537df-119">-ResourceGroupName</span></span>
<span data-ttu-id="537df-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="537df-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="537df-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="537df-121">-ServerName</span></span>
<span data-ttu-id="537df-122">Nazwa programu Azure SQL Server, w którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="537df-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="537df-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="537df-123">-Confirm</span></span>
<span data-ttu-id="537df-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="537df-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="537df-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="537df-125">-WhatIf</span></span>
<span data-ttu-id="537df-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="537df-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="537df-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="537df-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="537df-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="537df-128">CommonParameters</span></span>
<span data-ttu-id="537df-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="537df-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="537df-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="537df-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="537df-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="537df-131">INPUTS</span></span>

### <span data-ttu-id="537df-132">System. String</span><span class="sxs-lookup"><span data-stu-id="537df-132">System.String</span></span>

### <span data-ttu-id="537df-133">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="537df-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="537df-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="537df-134">OUTPUTS</span></span>

### <span data-ttu-id="537df-135">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="537df-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="537df-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="537df-136">NOTES</span></span>

## <span data-ttu-id="537df-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="537df-137">RELATED LINKS</span></span>
