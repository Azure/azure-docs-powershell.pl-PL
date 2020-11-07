---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: bc072934fe8695cae0fd5f5762c1a31936997da9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707971"
---
# <span data-ttu-id="5c94d-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="5c94d-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="5c94d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c94d-102">SYNOPSIS</span></span>
<span data-ttu-id="5c94d-103">Pobiera postęp TDEgo skanowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5c94d-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="5c94d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c94d-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c94d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5c94d-105">DESCRIPTION</span></span>
<span data-ttu-id="5c94d-106">Polecenie cmdlet **Get-AzSqlDatabaseTransparentDataEncryptionActivity umożliwia wyświetlenie** postępu skanowania przezroczystego szyfrowania danych (TDE) usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="5c94d-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="5c94d-107">Jeśli żaden zakres szyfrowania nie jest uruchomiony, to polecenie cmdlet zwraca pustą listę.</span><span class="sxs-lookup"><span data-stu-id="5c94d-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="5c94d-108">Aby uzyskać więcej informacji, zobacz przezroczyste szyfrowanie danych za pomocą usługi Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) w bibliotece Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="5c94d-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="5c94d-109">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5c94d-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5c94d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c94d-110">EXAMPLES</span></span>

### <span data-ttu-id="5c94d-111">Przykład 1: Pobieranie aktywności TDE dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="5c94d-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="5c94d-112">To polecenie pobiera aktywność TDE dla bazy danych o nazwie database01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="5c94d-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="5c94d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c94d-113">PARAMETERS</span></span>

### <span data-ttu-id="5c94d-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c94d-114">-DatabaseName</span></span>
<span data-ttu-id="5c94d-115">Określa nazwę bazy danych, dla której to polecenie cmdlet uzyskuje aktywność szyfrowania TDE.</span><span class="sxs-lookup"><span data-stu-id="5c94d-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="5c94d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c94d-116">-DefaultProfile</span></span>
<span data-ttu-id="5c94d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5c94d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c94d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c94d-118">-ResourceGroupName</span></span>
<span data-ttu-id="5c94d-119">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="5c94d-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5c94d-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="5c94d-120">-ServerName</span></span>
<span data-ttu-id="5c94d-121">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="5c94d-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="5c94d-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5c94d-122">-Confirm</span></span>
<span data-ttu-id="5c94d-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c94d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c94d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c94d-124">-WhatIf</span></span>
<span data-ttu-id="5c94d-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c94d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c94d-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5c94d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c94d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c94d-127">CommonParameters</span></span>
<span data-ttu-id="5c94d-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c94d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c94d-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c94d-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c94d-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c94d-130">INPUTS</span></span>

### <span data-ttu-id="5c94d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5c94d-131">System.String</span></span>

## <span data-ttu-id="5c94d-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c94d-132">OUTPUTS</span></span>

### <span data-ttu-id="5c94d-133">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="5c94d-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="5c94d-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c94d-134">NOTES</span></span>

## <span data-ttu-id="5c94d-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c94d-135">RELATED LINKS</span></span>

[<span data-ttu-id="5c94d-136">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="5c94d-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="5c94d-137">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="5c94d-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)

