---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40674DC7-E35F-4C9F-8CE0-D1C6F524C9FB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 1b4f72a5d57884975d6beb0d4676a0cbe5863681
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548508"
---
# <span data-ttu-id="af896-101">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="af896-101">Get-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="af896-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af896-102">SYNOPSIS</span></span>
<span data-ttu-id="af896-103">Pobiera zasady inspekcji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="af896-103">Gets the auditing policy of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af896-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af896-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditingPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af896-105">Opis</span><span class="sxs-lookup"><span data-stu-id="af896-105">DESCRIPTION</span></span>
<span data-ttu-id="af896-106">Polecenie cmdlet **Get-AzureRmSqlServerAuditingPolicy** pobiera zasady inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="af896-106">The **Get-AzureRmSqlServerAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="af896-107">Określ parametry *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* , które identyfikują bazę danych.</span><span class="sxs-lookup"><span data-stu-id="af896-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="af896-108">To polecenie cmdlet zwraca zasadę używaną przez bazy danych SQL Azure, które są zdefiniowane w określonym programie Azure SQL Server i używają jej zasad inspekcji.</span><span class="sxs-lookup"><span data-stu-id="af896-108">This cmdlet returns a policy that is used by the Azure SQL databases that are both defined in the specified Azure SQL server and use its auditing policy.</span></span>

## <span data-ttu-id="af896-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af896-109">EXAMPLES</span></span>

### <span data-ttu-id="af896-110">Przykład 1: uzyskiwanie zasad inspekcji programu Azure SQL Server z zdefiniowaną funkcją inspekcji tabeli</span><span class="sxs-lookup"><span data-stu-id="af896-110">Example 1: Get the auditing policy of an Azure SQL server with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
EventType              : {PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure...} 
TableIdentifier        : MyAuditTableName
FullAuditLogsTableName : SQLDBAuditLogsMyAuditTableName
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Table
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

### <span data-ttu-id="af896-111">Przykład 2: uzyskiwanie zasad inspekcji programu Azure SQL Server z zdefiniowaną funkcją inspekcji obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="af896-111">Example 2: Get the auditing policy of an Azure SQL server with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...} 
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Blob
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="af896-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af896-112">PARAMETERS</span></span>

### <span data-ttu-id="af896-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af896-113">-DefaultProfile</span></span>
<span data-ttu-id="af896-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="af896-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af896-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af896-115">-ResourceGroupName</span></span>
<span data-ttu-id="af896-116">Określa nazwę grupy zasobów, do której jest przypisany Program Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="af896-116">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="af896-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="af896-117">-ServerName</span></span>
<span data-ttu-id="af896-118">Określa nazwę programu Azure SQL Server, dla którego to polecenie cmdlet pobiera zasady inspekcji.</span><span class="sxs-lookup"><span data-stu-id="af896-118">Specifies the name of the Azure SQL server for which this cmdlet gets the auditing policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af896-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="af896-119">-Confirm</span></span>
<span data-ttu-id="af896-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af896-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af896-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af896-121">-WhatIf</span></span>
<span data-ttu-id="af896-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af896-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af896-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="af896-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af896-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af896-124">CommonParameters</span></span>
<span data-ttu-id="af896-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af896-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af896-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af896-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af896-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af896-127">INPUTS</span></span>

### <span data-ttu-id="af896-128">System. String</span><span class="sxs-lookup"><span data-stu-id="af896-128">System.String</span></span>

## <span data-ttu-id="af896-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af896-129">OUTPUTS</span></span>

### <span data-ttu-id="af896-130">Microsoft. Azure. Commands. SQL. Audit. model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="af896-130">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="af896-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af896-131">NOTES</span></span>

## <span data-ttu-id="af896-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af896-132">RELATED LINKS</span></span>

[<span data-ttu-id="af896-133">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="af896-133">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="af896-134">Użyj — AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="af896-134">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="af896-135">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="af896-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


