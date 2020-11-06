---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 999fd83af11422f1499e386f194fd75d9b99e152
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543320"
---
# <span data-ttu-id="99f48-101">Stop-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="99f48-101">Stop-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="99f48-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99f48-102">SYNOPSIS</span></span>
<span data-ttu-id="99f48-103">Anuluje operację aktualizacji asynchronicznej w puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="99f48-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99f48-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99f48-104">SYNTAX</span></span>

```
Stop-AzureRmSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99f48-105">Opis</span><span class="sxs-lookup"><span data-stu-id="99f48-105">DESCRIPTION</span></span>
<span data-ttu-id="99f48-106">Polecenie cmdlet **stop-AzureRmSqlElasticPoolActivity** anuluje operację aktualizacji asynchronicznej w puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="99f48-106">The **Stop-AzureRmSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="99f48-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99f48-107">EXAMPLES</span></span>

### <span data-ttu-id="99f48-108">Przykład 1. Anuluj operację aktualizacji asynchronicznej w puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="99f48-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

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

<span data-ttu-id="99f48-109">To polecenie anuluje operację aktualizacji asynchronicznych na puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="99f48-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="99f48-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99f48-110">PARAMETERS</span></span>

### <span data-ttu-id="99f48-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f48-111">-DefaultProfile</span></span>
<span data-ttu-id="99f48-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="99f48-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f48-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="99f48-113">-ElasticPoolName</span></span>
<span data-ttu-id="99f48-114">Nazwa puli elastycznej SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="99f48-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="99f48-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="99f48-115">-OperationId</span></span>
<span data-ttu-id="99f48-116">Identyfikator operacji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="99f48-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="99f48-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99f48-117">-PassThru</span></span>
<span data-ttu-id="99f48-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="99f48-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="99f48-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f48-119">-ResourceGroupName</span></span>
<span data-ttu-id="99f48-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="99f48-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="99f48-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="99f48-121">-ServerName</span></span>
<span data-ttu-id="99f48-122">Nazwa programu Azure SQL Server, w którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="99f48-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="99f48-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99f48-123">-Confirm</span></span>
<span data-ttu-id="99f48-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99f48-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99f48-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99f48-125">-WhatIf</span></span>
<span data-ttu-id="99f48-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99f48-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99f48-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="99f48-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99f48-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f48-128">CommonParameters</span></span>
<span data-ttu-id="99f48-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99f48-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f48-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99f48-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f48-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99f48-131">INPUTS</span></span>

### <span data-ttu-id="99f48-132">System. String</span><span class="sxs-lookup"><span data-stu-id="99f48-132">System.String</span></span>

### <span data-ttu-id="99f48-133">System. Nullable "1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="99f48-133">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="99f48-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99f48-134">OUTPUTS</span></span>

### <span data-ttu-id="99f48-135">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="99f48-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="99f48-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99f48-136">NOTES</span></span>

## <span data-ttu-id="99f48-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99f48-137">RELATED LINKS</span></span>
