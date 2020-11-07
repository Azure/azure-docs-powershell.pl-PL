---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 8d89b966da0fc9d5f0517c5faf777cb5d16efc33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707746"
---
# <span data-ttu-id="90fad-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="90fad-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="90fad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90fad-102">SYNOPSIS</span></span>
<span data-ttu-id="90fad-103">Modyfikuje Właściwość TDE bazy danych.</span><span class="sxs-lookup"><span data-stu-id="90fad-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="90fad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90fad-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90fad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="90fad-105">DESCRIPTION</span></span>
<span data-ttu-id="90fad-106">Polecenie cmdlet **Set-AzSqlDatabaseTransparentDataEncryption** modyfikuje Właściwość przezroczystego szyfrowania danych (TDE) bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="90fad-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="90fad-107">Aby uzyskać więcej informacji, zobacz przezroczyste szyfrowanie danych za pomocą usługi Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) w bibliotece Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="90fad-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="90fad-108">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="90fad-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="90fad-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90fad-109">EXAMPLES</span></span>

### <span data-ttu-id="90fad-110">Przykład 1: Włączanie TDE dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="90fad-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="90fad-111">To polecenie włącza TDE dla bazy danych o nazwie Database01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="90fad-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="90fad-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90fad-112">PARAMETERS</span></span>

### <span data-ttu-id="90fad-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="90fad-113">-DatabaseName</span></span>
<span data-ttu-id="90fad-114">Określa nazwę bazy danych modyfikowanej przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90fad-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="90fad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90fad-115">-DefaultProfile</span></span>
<span data-ttu-id="90fad-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="90fad-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90fad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90fad-117">-ResourceGroupName</span></span>
<span data-ttu-id="90fad-118">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="90fad-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="90fad-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="90fad-119">-ServerName</span></span>
<span data-ttu-id="90fad-120">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="90fad-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="90fad-121">-State</span><span class="sxs-lookup"><span data-stu-id="90fad-121">-State</span></span>
<span data-ttu-id="90fad-122">Określa wartość właściwości TDE.</span><span class="sxs-lookup"><span data-stu-id="90fad-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="90fad-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="90fad-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="90fad-124">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="90fad-124">Enabled</span></span> 
- <span data-ttu-id="90fad-125">Łącza</span><span class="sxs-lookup"><span data-stu-id="90fad-125">Disabled</span></span>

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

### <span data-ttu-id="90fad-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90fad-126">-Confirm</span></span>
<span data-ttu-id="90fad-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90fad-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90fad-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90fad-128">-WhatIf</span></span>
<span data-ttu-id="90fad-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90fad-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90fad-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="90fad-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90fad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90fad-131">CommonParameters</span></span>
<span data-ttu-id="90fad-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90fad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90fad-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90fad-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90fad-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90fad-134">INPUTS</span></span>

### <span data-ttu-id="90fad-135">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="90fad-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="90fad-136">System. String</span><span class="sxs-lookup"><span data-stu-id="90fad-136">System.String</span></span>

## <span data-ttu-id="90fad-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90fad-137">OUTPUTS</span></span>

### <span data-ttu-id="90fad-138">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="90fad-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="90fad-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90fad-139">NOTES</span></span>

## <span data-ttu-id="90fad-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90fad-140">RELATED LINKS</span></span>

[<span data-ttu-id="90fad-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="90fad-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="90fad-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="90fad-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="90fad-143">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="90fad-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

