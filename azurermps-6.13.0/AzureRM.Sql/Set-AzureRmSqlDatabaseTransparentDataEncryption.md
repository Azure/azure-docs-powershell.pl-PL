---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: ec35e0ebd0f674c66b7708289c33253b28219433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552003"
---
# <span data-ttu-id="b1efa-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="b1efa-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="b1efa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1efa-102">SYNOPSIS</span></span>
<span data-ttu-id="b1efa-103">Modyfikuje Właściwość TDE bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b1efa-103">Modifies TDE property for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1efa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1efa-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1efa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b1efa-105">DESCRIPTION</span></span>
<span data-ttu-id="b1efa-106">Polecenie cmdlet **Set-AzureRmSqlDatabaseTransparentDataEncryption** modyfikuje Właściwość przezroczystego szyfrowania danych (TDE) bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b1efa-106">The **Set-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="b1efa-107">Aby uzyskać więcej informacji, zobacz przezroczyste szyfrowanie danych za pomocą usługi Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) w bibliotece Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="b1efa-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="b1efa-108">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="b1efa-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b1efa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1efa-109">EXAMPLES</span></span>

### <span data-ttu-id="b1efa-110">Przykład 1: Włączanie TDE dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="b1efa-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="b1efa-111">To polecenie włącza TDE dla bazy danych o nazwie Database01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="b1efa-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="b1efa-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1efa-112">PARAMETERS</span></span>

### <span data-ttu-id="b1efa-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b1efa-113">-DatabaseName</span></span>
<span data-ttu-id="b1efa-114">Określa nazwę bazy danych modyfikowanej przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1efa-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b1efa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1efa-115">-DefaultProfile</span></span>
<span data-ttu-id="b1efa-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b1efa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1efa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1efa-117">-ResourceGroupName</span></span>
<span data-ttu-id="b1efa-118">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="b1efa-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="b1efa-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b1efa-119">-ServerName</span></span>
<span data-ttu-id="b1efa-120">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="b1efa-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="b1efa-121">-State</span><span class="sxs-lookup"><span data-stu-id="b1efa-121">-State</span></span>
<span data-ttu-id="b1efa-122">Określa wartość właściwości TDE.</span><span class="sxs-lookup"><span data-stu-id="b1efa-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="b1efa-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b1efa-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b1efa-124">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="b1efa-124">Enabled</span></span> 
- <span data-ttu-id="b1efa-125">Łącza</span><span class="sxs-lookup"><span data-stu-id="b1efa-125">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1efa-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b1efa-126">-Confirm</span></span>
<span data-ttu-id="b1efa-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1efa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1efa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1efa-128">-WhatIf</span></span>
<span data-ttu-id="b1efa-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1efa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1efa-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b1efa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1efa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1efa-131">CommonParameters</span></span>
<span data-ttu-id="b1efa-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1efa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1efa-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1efa-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1efa-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1efa-134">INPUTS</span></span>

### <span data-ttu-id="b1efa-135">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="b1efa-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="b1efa-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b1efa-136">System.String</span></span>

## <span data-ttu-id="b1efa-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1efa-137">OUTPUTS</span></span>

### <span data-ttu-id="b1efa-138">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="b1efa-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="b1efa-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1efa-139">NOTES</span></span>

## <span data-ttu-id="b1efa-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1efa-140">RELATED LINKS</span></span>

[<span data-ttu-id="b1efa-141">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="b1efa-141">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="b1efa-142">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="b1efa-142">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="b1efa-143">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b1efa-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


