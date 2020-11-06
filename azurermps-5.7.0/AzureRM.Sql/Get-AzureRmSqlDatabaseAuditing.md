---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 9058863da0af6addd243f5e7ec544a8dad7b3b03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524873"
---
# <span data-ttu-id="0f943-101">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="0f943-101">Get-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="0f943-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f943-102">SYNOPSIS</span></span>
<span data-ttu-id="0f943-103">Pobiera ustawienia inspekcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0f943-103">Gets the auditing settings of an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f943-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f943-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditing [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f943-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0f943-105">DESCRIPTION</span></span>
<span data-ttu-id="0f943-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseAuditing** pobiera ustawienia inspekcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0f943-106">The **Get-AzureRmSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="0f943-107">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0f943-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="0f943-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f943-108">EXAMPLES</span></span>

### <span data-ttu-id="0f943-109">Przykład 1: uzyskiwanie ustawień inspekcji bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="0f943-109">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
AuditAction            : {}
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...}
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="0f943-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f943-110">PARAMETERS</span></span>

### <span data-ttu-id="0f943-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0f943-111">-DatabaseName</span></span>
<span data-ttu-id="0f943-112">Nazwa bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="0f943-112">SQL Database name.</span></span>

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

### <span data-ttu-id="0f943-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f943-113">-DefaultProfile</span></span>
<span data-ttu-id="0f943-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0f943-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f943-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f943-115">-ResourceGroupName</span></span>
<span data-ttu-id="0f943-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0f943-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="0f943-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0f943-117">-ServerName</span></span>
<span data-ttu-id="0f943-118">Nazwa serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="0f943-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="0f943-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f943-119">-Confirm</span></span>
<span data-ttu-id="0f943-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f943-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f943-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f943-121">-WhatIf</span></span>
<span data-ttu-id="0f943-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f943-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f943-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0f943-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f943-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f943-124">CommonParameters</span></span>
<span data-ttu-id="0f943-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f943-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f943-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f943-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f943-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f943-127">INPUTS</span></span>

### <span data-ttu-id="0f943-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0f943-128">None</span></span>
<span data-ttu-id="0f943-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="0f943-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0f943-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f943-130">OUTPUTS</span></span>

### <span data-ttu-id="0f943-131">Microsoft. Azure. Commands. SQL. Security. model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="0f943-131">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="0f943-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f943-132">NOTES</span></span>

## <span data-ttu-id="0f943-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f943-133">RELATED LINKS</span></span>
