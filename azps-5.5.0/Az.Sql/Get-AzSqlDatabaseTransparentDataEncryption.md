---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 632b7710a6055f40c6cdc6d87d4b2cf8e3e17eeb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178515"
---
# <span data-ttu-id="9f4e3-101">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="9f4e3-101">Get-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="9f4e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f4e3-102">SYNOPSIS</span></span>
<span data-ttu-id="9f4e3-103">Pobiera stan TDE dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-103">Gets the TDE state for a database.</span></span>

## <span data-ttu-id="9f4e3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9f4e3-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f4e3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9f4e3-105">DESCRIPTION</span></span>
<span data-ttu-id="9f4e3-106">Polecenie **cmdlet Get-AzSqlDatabaseTransparentDataEncryption** pobiera stan transparentnego szyfrowania danych (TDE, Transparent Data Encryption) dla bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-106">The **Get-AzSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="9f4e3-107">Aby uzyskać więcej informacji, zobacz przezroczyste szyfrowanie danych przy użyciu usługi Azure SQL Database https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) (w bibliotece Microsoft Developer Network Library).</span><span class="sxs-lookup"><span data-stu-id="9f4e3-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="9f4e3-108">To polecenie cmdlet uzyskuje bieżący stan TDE, ale zarówno szyfrowanie, jak i odszyfrowywanie mogą być operacjami długotrwałym.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="9f4e3-109">Aby wyświetlić postęp skanowania szyfrowania, uruchom Get-AzSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-109">To see the encryption scan progress, run the Get-AzSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="9f4e3-110">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="9f4e3-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9f4e3-111">EXAMPLES</span></span>

### <span data-ttu-id="9f4e3-112">Przykład 1. Uzyskiwanie stanu TDE dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="9f4e3-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="9f4e3-113">To polecenie pobiera stan TDE dla bazy danych o nazwie Database01 na serwerze o nazwie serwer01.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="9f4e3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f4e3-114">PARAMETERS</span></span>

### <span data-ttu-id="9f4e3-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9f4e3-115">-DatabaseName</span></span>
<span data-ttu-id="9f4e3-116">Określa nazwę bazy danych, dla której to polecenie cmdlet ma stan TDE.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="9f4e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f4e3-117">-DefaultProfile</span></span>
<span data-ttu-id="9f4e3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9f4e3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f4e3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f4e3-119">-ResourceGroupName</span></span>
<span data-ttu-id="9f4e3-120">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="9f4e3-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9f4e3-121">-ServerName</span></span>
<span data-ttu-id="9f4e3-122">Określa nazwę serwera hostatora bazy danych, dla którego to polecenie cmdlet ma stan TDE.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="9f4e3-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9f4e3-123">-Confirm</span></span>
<span data-ttu-id="9f4e3-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f4e3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f4e3-125">-WhatIf</span></span>
<span data-ttu-id="9f4e3-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f4e3-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f4e3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f4e3-128">CommonParameters</span></span>
<span data-ttu-id="9f4e3-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f4e3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f4e3-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f4e3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f4e3-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f4e3-131">INPUTS</span></span>

### <span data-ttu-id="9f4e3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9f4e3-132">System.String</span></span>

## <span data-ttu-id="9f4e3-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f4e3-133">OUTPUTS</span></span>

### <span data-ttu-id="9f4e3-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="9f4e3-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="9f4e3-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9f4e3-135">NOTES</span></span>

## <span data-ttu-id="9f4e3-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f4e3-136">RELATED LINKS</span></span>

[<span data-ttu-id="9f4e3-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="9f4e3-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="9f4e3-138">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="9f4e3-138">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)
