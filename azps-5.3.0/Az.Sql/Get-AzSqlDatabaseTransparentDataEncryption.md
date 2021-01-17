---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 632b7710a6055f40c6cdc6d87d4b2cf8e3e17eeb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489362"
---
# <span data-ttu-id="c9900-101">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="c9900-101">Get-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="c9900-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9900-102">SYNOPSIS</span></span>
<span data-ttu-id="c9900-103">Pobiera stan TDE bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c9900-103">Gets the TDE state for a database.</span></span>

## <span data-ttu-id="c9900-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9900-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9900-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c9900-105">DESCRIPTION</span></span>
<span data-ttu-id="c9900-106">Polecenie cmdlet **Get-AzSqlDatabaseTransparentDataEncryption** Pobiera stan przezroczystego szyfrowania danych (TDE) dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c9900-106">The **Get-AzSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="c9900-107">Aby uzyskać więcej informacji, zobacz przezroczyste szyfrowanie danych za pomocą usługi Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) w bibliotece Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="c9900-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="c9900-108">To polecenie cmdlet pobiera bieżący stan TDE, ale zarówno szyfrowanie, jak i odszyfrowywanie mogą być długotrwałymi operacjami.</span><span class="sxs-lookup"><span data-stu-id="c9900-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="c9900-109">Aby wyświetlić postęp skanowania w postaci szyfrowania, uruchom polecenie cmdlet Get-AzSqlDatabaseTransparentDataEncryptionActivity.</span><span class="sxs-lookup"><span data-stu-id="c9900-109">To see the encryption scan progress, run the Get-AzSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="c9900-110">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="c9900-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c9900-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9900-111">EXAMPLES</span></span>

### <span data-ttu-id="c9900-112">Przykład 1: uzyskiwanie statusu TDE dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="c9900-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="c9900-113">To polecenie uzyskuje stan TDE dla bazy danych o nazwie Database01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="c9900-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="c9900-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9900-114">PARAMETERS</span></span>

### <span data-ttu-id="c9900-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c9900-115">-DatabaseName</span></span>
<span data-ttu-id="c9900-116">Określa nazwę bazy danych, dla której to polecenie cmdlet pobiera stan TDE.</span><span class="sxs-lookup"><span data-stu-id="c9900-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="c9900-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9900-117">-DefaultProfile</span></span>
<span data-ttu-id="c9900-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c9900-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9900-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9900-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9900-120">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="c9900-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c9900-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c9900-121">-ServerName</span></span>
<span data-ttu-id="c9900-122">Określa nazwę serwera obsługującego bazę danych, dla której to polecenie cmdlet pobiera stan TDE.</span><span class="sxs-lookup"><span data-stu-id="c9900-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="c9900-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9900-123">-Confirm</span></span>
<span data-ttu-id="c9900-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9900-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9900-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9900-125">-WhatIf</span></span>
<span data-ttu-id="c9900-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9900-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9900-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c9900-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9900-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9900-128">CommonParameters</span></span>
<span data-ttu-id="c9900-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9900-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9900-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9900-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9900-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9900-131">INPUTS</span></span>

### <span data-ttu-id="c9900-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c9900-132">System.String</span></span>

## <span data-ttu-id="c9900-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9900-133">OUTPUTS</span></span>

### <span data-ttu-id="c9900-134">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="c9900-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="c9900-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9900-135">NOTES</span></span>

## <span data-ttu-id="c9900-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9900-136">RELATED LINKS</span></span>

[<span data-ttu-id="c9900-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="c9900-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="c9900-138">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="c9900-138">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)
