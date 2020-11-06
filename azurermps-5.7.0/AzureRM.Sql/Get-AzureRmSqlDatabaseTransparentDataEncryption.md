---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 5136da99879e4636018ae1a01cc95f39f2924b4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547920"
---
# <span data-ttu-id="4128a-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4128a-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="4128a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4128a-102">SYNOPSIS</span></span>
<span data-ttu-id="4128a-103">Pobiera stan TDE bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4128a-103">Gets the TDE state for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4128a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4128a-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4128a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4128a-105">DESCRIPTION</span></span>
<span data-ttu-id="4128a-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseTransparentDataEncryption** Pobiera stan przezroczystego szyfrowania danych (TDE) dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4128a-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="4128a-107">Aby uzyskać więcej informacji, zobacz przezroczyste szyfrowanie danych za pomocą usługi Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) w bibliotece Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="4128a-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="4128a-108">To polecenie cmdlet pobiera bieżący stan TDE, ale zarówno szyfrowanie, jak i odszyfrowywanie mogą być długotrwałymi operacjami.</span><span class="sxs-lookup"><span data-stu-id="4128a-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="4128a-109">Aby wyświetlić postęp skanowania w postaci szyfrowania, uruchom polecenie cmdlet Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.</span><span class="sxs-lookup"><span data-stu-id="4128a-109">To see the encryption scan progress, run the Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>

<span data-ttu-id="4128a-110">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="4128a-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4128a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4128a-111">EXAMPLES</span></span>

### <span data-ttu-id="4128a-112">Przykład 1: uzyskiwanie statusu TDE dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="4128a-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="4128a-113">To polecenie uzyskuje stan TDE dla bazy danych o nazwie Database01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="4128a-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="4128a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4128a-114">PARAMETERS</span></span>

### <span data-ttu-id="4128a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4128a-115">-DatabaseName</span></span>
<span data-ttu-id="4128a-116">Określa nazwę bazy danych, dla której to polecenie cmdlet pobiera stan TDE.</span><span class="sxs-lookup"><span data-stu-id="4128a-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="4128a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4128a-117">-DefaultProfile</span></span>
<span data-ttu-id="4128a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4128a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4128a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4128a-119">-ResourceGroupName</span></span>
<span data-ttu-id="4128a-120">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="4128a-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="4128a-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4128a-121">-ServerName</span></span>
<span data-ttu-id="4128a-122">Określa nazwę serwera obsługującego bazę danych, dla której to polecenie cmdlet pobiera stan TDE.</span><span class="sxs-lookup"><span data-stu-id="4128a-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="4128a-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4128a-123">-Confirm</span></span>
<span data-ttu-id="4128a-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4128a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4128a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4128a-125">-WhatIf</span></span>
<span data-ttu-id="4128a-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4128a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4128a-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4128a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4128a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4128a-128">CommonParameters</span></span>
<span data-ttu-id="4128a-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4128a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4128a-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4128a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4128a-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4128a-131">INPUTS</span></span>

### <span data-ttu-id="4128a-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4128a-132">None</span></span>
<span data-ttu-id="4128a-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4128a-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4128a-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4128a-134">OUTPUTS</span></span>

### <span data-ttu-id="4128a-135">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="4128a-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="4128a-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4128a-136">NOTES</span></span>

## <span data-ttu-id="4128a-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4128a-137">RELATED LINKS</span></span>

[<span data-ttu-id="4128a-138">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="4128a-138">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="4128a-139">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4128a-139">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)
