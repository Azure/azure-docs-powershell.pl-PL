---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: ca3ee787e577eabc9e889cbb471fcf3a00a4736c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716864"
---
# <span data-ttu-id="4e3e0-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4e3e0-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="4e3e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e3e0-102">SYNOPSIS</span></span>
<span data-ttu-id="4e3e0-103">Modyfikuje Właściwość TDE bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4e3e0-103">Modifies TDE property for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e3e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e3e0-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e3e0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4e3e0-105">DESCRIPTION</span></span>
<span data-ttu-id="4e3e0-106">Polecenie cmdlet **Set-AzureRmSqlDatabaseTransparentDataEncryption** modyfikuje Właściwość przezroczystego szyfrowania danych (TDE) bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4e3e0-106">The **Set-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="4e3e0-107">Aby uzyskać więcej informacji, zobacz przezroczyste szyfrowanie danych za pomocą usługi Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) w bibliotece Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="4e3e0-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="4e3e0-108">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="4e3e0-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4e3e0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e3e0-109">EXAMPLES</span></span>

### <span data-ttu-id="4e3e0-110">Przykład 1: Włączanie TDE dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="4e3e0-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="4e3e0-111">To polecenie włącza TDE dla bazy danych o nazwie Database01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="4e3e0-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="4e3e0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e3e0-112">PARAMETERS</span></span>

### <span data-ttu-id="4e3e0-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e3e0-113">-DatabaseName</span></span>
<span data-ttu-id="4e3e0-114">Określa nazwę bazy danych modyfikowanej przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e3e0-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4e3e0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e3e0-115">-ResourceGroupName</span></span>
<span data-ttu-id="4e3e0-116">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="4e3e0-116">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="4e3e0-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4e3e0-117">-ServerName</span></span>
<span data-ttu-id="4e3e0-118">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="4e3e0-118">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="4e3e0-119">-State</span><span class="sxs-lookup"><span data-stu-id="4e3e0-119">-State</span></span>
<span data-ttu-id="4e3e0-120">Określa wartość właściwości TDE.</span><span class="sxs-lookup"><span data-stu-id="4e3e0-120">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="4e3e0-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4e3e0-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4e3e0-122">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="4e3e0-122">Enabled</span></span> 
- <span data-ttu-id="4e3e0-123">Łącza</span><span class="sxs-lookup"><span data-stu-id="4e3e0-123">Disabled</span></span>

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

### <span data-ttu-id="4e3e0-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4e3e0-124">-Confirm</span></span>
<span data-ttu-id="4e3e0-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e3e0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e3e0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e3e0-126">-WhatIf</span></span>
<span data-ttu-id="4e3e0-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e3e0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e3e0-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4e3e0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e3e0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e3e0-129">-DefaultProfile</span></span>
<span data-ttu-id="4e3e0-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e3e0-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e3e0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e3e0-131">CommonParameters</span></span>
<span data-ttu-id="4e3e0-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e3e0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e3e0-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e3e0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e3e0-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e3e0-134">INPUTS</span></span>

## <span data-ttu-id="4e3e0-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e3e0-135">OUTPUTS</span></span>

### <span data-ttu-id="4e3e0-136">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="4e3e0-136">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="4e3e0-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e3e0-137">NOTES</span></span>

## <span data-ttu-id="4e3e0-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e3e0-138">RELATED LINKS</span></span>

[<span data-ttu-id="4e3e0-139">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4e3e0-139">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="4e3e0-140">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="4e3e0-140">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="4e3e0-141">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="4e3e0-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


