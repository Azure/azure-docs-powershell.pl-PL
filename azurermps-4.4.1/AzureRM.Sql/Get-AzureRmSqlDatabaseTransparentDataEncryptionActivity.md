---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: 0f858e2ad0260995b71ec6146a6ce7e64bd48c29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716739"
---
# <span data-ttu-id="752ae-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="752ae-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="752ae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="752ae-102">SYNOPSIS</span></span>
<span data-ttu-id="752ae-103">Pobiera postęp TDEgo skanowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="752ae-103">Gets the progress of a TDE scan of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="752ae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="752ae-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="752ae-105">Opis</span><span class="sxs-lookup"><span data-stu-id="752ae-105">DESCRIPTION</span></span>
<span data-ttu-id="752ae-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity umożliwia wyświetlenie** postępu skanowania przezroczystego szyfrowania danych (TDE) usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="752ae-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="752ae-107">Jeśli żaden zakres szyfrowania nie jest uruchomiony, to polecenie cmdlet zwraca pustą listę.</span><span class="sxs-lookup"><span data-stu-id="752ae-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="752ae-108">Aby uzyskać więcej informacji, zobacz przezroczyste szyfrowanie danych za pomocą usługi Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) w bibliotece Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="752ae-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="752ae-109">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="752ae-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="752ae-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="752ae-110">EXAMPLES</span></span>

### <span data-ttu-id="752ae-111">Przykład 1: Pobieranie aktywności TDE dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="752ae-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="752ae-112">To polecenie pobiera aktywność TDE dla bazy danych o nazwie database01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="752ae-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="752ae-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="752ae-113">PARAMETERS</span></span>

### <span data-ttu-id="752ae-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="752ae-114">-DatabaseName</span></span>
<span data-ttu-id="752ae-115">Określa nazwę bazy danych, dla której to polecenie cmdlet uzyskuje aktywność szyfrowania TDE.</span><span class="sxs-lookup"><span data-stu-id="752ae-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="752ae-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="752ae-116">-ResourceGroupName</span></span>
<span data-ttu-id="752ae-117">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="752ae-117">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="752ae-118">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="752ae-118">-ServerName</span></span>
<span data-ttu-id="752ae-119">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="752ae-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="752ae-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="752ae-120">-Confirm</span></span>
<span data-ttu-id="752ae-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="752ae-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="752ae-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="752ae-122">-WhatIf</span></span>
<span data-ttu-id="752ae-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="752ae-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="752ae-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="752ae-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="752ae-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="752ae-125">-DefaultProfile</span></span>
<span data-ttu-id="752ae-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="752ae-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="752ae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="752ae-127">CommonParameters</span></span>
<span data-ttu-id="752ae-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="752ae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="752ae-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="752ae-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="752ae-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="752ae-130">INPUTS</span></span>

## <span data-ttu-id="752ae-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="752ae-131">OUTPUTS</span></span>

### <span data-ttu-id="752ae-132">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="752ae-132">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="752ae-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="752ae-133">NOTES</span></span>

## <span data-ttu-id="752ae-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="752ae-134">RELATED LINKS</span></span>

[<span data-ttu-id="752ae-135">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="752ae-135">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="752ae-136">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="752ae-136">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)


