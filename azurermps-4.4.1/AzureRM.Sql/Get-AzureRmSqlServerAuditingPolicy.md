---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40674DC7-E35F-4C9F-8CE0-D1C6F524C9FB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 34eedd81d5e8625ed957cba16d3cec1ea33a0c32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545968"
---
# <span data-ttu-id="d234b-101">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d234b-101">Get-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="d234b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d234b-102">SYNOPSIS</span></span>
<span data-ttu-id="d234b-103">Pobiera zasady inspekcji programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d234b-103">Gets the auditing policy of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d234b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d234b-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditingPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d234b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d234b-105">DESCRIPTION</span></span>
<span data-ttu-id="d234b-106">Polecenie cmdlet **Get-AzureRmSqlServerAuditingPolicy** pobiera zasady inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d234b-106">The **Get-AzureRmSqlServerAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="d234b-107">Określ parametry *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* , które identyfikują bazę danych.</span><span class="sxs-lookup"><span data-stu-id="d234b-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="d234b-108">To polecenie cmdlet zwraca zasadę używaną przez bazy danych SQL Azure, które są zdefiniowane w określonym programie Azure SQL Server i używają jej zasad inspekcji.</span><span class="sxs-lookup"><span data-stu-id="d234b-108">This cmdlet returns a policy that is used by the Azure SQL databases that are both defined in the specified Azure SQL server and use its auditing policy.</span></span>

## <span data-ttu-id="d234b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d234b-109">EXAMPLES</span></span>

### <span data-ttu-id="d234b-110">Przykład 1: uzyskiwanie zasad inspekcji programu Azure SQL Server z zdefiniowaną funkcją inspekcji tabeli</span><span class="sxs-lookup"><span data-stu-id="d234b-110">Example 1: Get the auditing policy of an Azure SQL server with Table auditing defined on it</span></span>
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

### <span data-ttu-id="d234b-111">Przykład 2: uzyskiwanie zasad inspekcji programu Azure SQL Server z zdefiniowaną funkcją inspekcji obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="d234b-111">Example 2: Get the auditing policy of an Azure SQL server with Blob auditing defined on it</span></span>
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

## <span data-ttu-id="d234b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d234b-112">PARAMETERS</span></span>

### <span data-ttu-id="d234b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d234b-113">-ResourceGroupName</span></span>
<span data-ttu-id="d234b-114">Określa nazwę grupy zasobów, do której jest przypisany Program Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d234b-114">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="d234b-115">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d234b-115">-ServerName</span></span>
<span data-ttu-id="d234b-116">Określa nazwę programu Azure SQL Server, dla którego to polecenie cmdlet pobiera zasady inspekcji.</span><span class="sxs-lookup"><span data-stu-id="d234b-116">Specifies the name of the Azure SQL server for which this cmdlet gets the auditing policy.</span></span>

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

### <span data-ttu-id="d234b-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d234b-117">-Confirm</span></span>
<span data-ttu-id="d234b-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d234b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d234b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d234b-119">-WhatIf</span></span>
<span data-ttu-id="d234b-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d234b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d234b-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d234b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d234b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d234b-122">-DefaultProfile</span></span>
<span data-ttu-id="d234b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d234b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d234b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d234b-124">CommonParameters</span></span>
<span data-ttu-id="d234b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d234b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d234b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d234b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d234b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d234b-127">INPUTS</span></span>

## <span data-ttu-id="d234b-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d234b-128">OUTPUTS</span></span>

### <span data-ttu-id="d234b-129">Microsoft. Azure. Commands. SQL. Security. model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d234b-129">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="d234b-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d234b-130">NOTES</span></span>

## <span data-ttu-id="d234b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d234b-131">RELATED LINKS</span></span>

[<span data-ttu-id="d234b-132">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d234b-132">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="d234b-133">Użyj — AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d234b-133">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="d234b-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="d234b-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


