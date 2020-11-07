---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 4d15400da4105f719f5948a53512f6c33cbd3bd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718008"
---
# <span data-ttu-id="61f20-101">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="61f20-101">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="61f20-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61f20-102">SYNOPSIS</span></span>
<span data-ttu-id="61f20-103">Pobiera zasady inspekcji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="61f20-103">Gets the auditing policy of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61f20-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61f20-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61f20-105">Opis</span><span class="sxs-lookup"><span data-stu-id="61f20-105">DESCRIPTION</span></span>
<span data-ttu-id="61f20-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseAuditingPolicy** pobiera zasady inspekcji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="61f20-106">The **Get-AzureRmSqlDatabaseAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL Database.</span></span>
<span data-ttu-id="61f20-107">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="61f20-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="61f20-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61f20-108">EXAMPLES</span></span>

### <span data-ttu-id="61f20-109">Przykład 1: uzyskiwanie zasad inspekcji bazy danych SQL Azure z zdefiniowaną funkcją inspekcji tabeli</span><span class="sxs-lookup"><span data-stu-id="61f20-109">Example 1: Get the auditing policy of an Azure SQL database with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
UseServerDefault       : Disabled
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

### <span data-ttu-id="61f20-110">Przykład 2: uzyskiwanie zasad inspekcji bazy danych SQL Azure z zdefiniowaną funkcją inspekcji obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="61f20-110">Example 2: Get the auditing policy of an Azure SQL database with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
AuditAction            : {}
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

## <span data-ttu-id="61f20-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61f20-111">PARAMETERS</span></span>

### <span data-ttu-id="61f20-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="61f20-112">-DatabaseName</span></span>
<span data-ttu-id="61f20-113">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="61f20-113">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f20-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f20-114">-DefaultProfile</span></span>
<span data-ttu-id="61f20-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="61f20-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f20-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61f20-116">-ResourceGroupName</span></span>
<span data-ttu-id="61f20-117">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="61f20-117">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f20-118">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="61f20-118">-ServerName</span></span>
<span data-ttu-id="61f20-119">Określa nazwę serwera, na którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="61f20-119">Specifies the name of the server where the database is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f20-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61f20-120">-Confirm</span></span>
<span data-ttu-id="61f20-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61f20-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f20-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61f20-122">-WhatIf</span></span>
<span data-ttu-id="61f20-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61f20-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61f20-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="61f20-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f20-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f20-125">CommonParameters</span></span>
<span data-ttu-id="61f20-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61f20-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f20-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61f20-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f20-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61f20-128">INPUTS</span></span>

### <span data-ttu-id="61f20-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="61f20-129">None</span></span>
<span data-ttu-id="61f20-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="61f20-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61f20-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61f20-131">OUTPUTS</span></span>

### <span data-ttu-id="61f20-132">Microsoft. Azure. Commands. SQL. Security. model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="61f20-132">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="61f20-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61f20-133">NOTES</span></span>

## <span data-ttu-id="61f20-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61f20-134">RELATED LINKS</span></span>

[<span data-ttu-id="61f20-135">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="61f20-135">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="61f20-136">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="61f20-136">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)



