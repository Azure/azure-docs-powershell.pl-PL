---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: 3b63aea46cbff930303f8f8e58a66923a6df46b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528202"
---
# <span data-ttu-id="2474e-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2474e-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="2474e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2474e-102">SYNOPSIS</span></span>
<span data-ttu-id="2474e-103">Pobiera zasady bezpiecznego połączenia z bazą danych.</span><span class="sxs-lookup"><span data-stu-id="2474e-103">Gets the secure connection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2474e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2474e-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2474e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2474e-105">DESCRIPTION</span></span>
<span data-ttu-id="2474e-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseSecureConnectionPolicy** pobiera zasady zaszyfrowanego kanału bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2474e-106">The **Get-AzureRmSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="2474e-107">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2474e-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="2474e-108">Po pomyślnym uruchomieniu tego polecenia cmdlet zwróci on obiekt opisujący bieżące zasady zaszyfrowanego kanału, a także identyfikatory bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2474e-108">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="2474e-109">Identyfikatory bazy danych obejmują, ale nie są ograniczone do, **ResourceGroupName** , **nazwa_serwera** i **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="2474e-109">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="2474e-110">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2474e-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="2474e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2474e-111">EXAMPLES</span></span>

### <span data-ttu-id="2474e-112">Przykład 1: uzyskiwanie zasad zaszyfrowanego kanału bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="2474e-112">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

<span data-ttu-id="2474e-113">To polecenie pobiera zasady zaszyfrowanego kanału bazy danych Azure SQL Database o nazwie database01 znajdującej się na serwerze Server01.</span><span class="sxs-lookup"><span data-stu-id="2474e-113">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="2474e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2474e-114">PARAMETERS</span></span>

### <span data-ttu-id="2474e-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2474e-115">-DatabaseName</span></span>
<span data-ttu-id="2474e-116">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2474e-116">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="2474e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2474e-117">-ResourceGroupName</span></span>
<span data-ttu-id="2474e-118">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="2474e-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="2474e-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="2474e-119">-ServerName</span></span>
<span data-ttu-id="2474e-120">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="2474e-120">Specifies the name of server that hosts the database.</span></span>

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

### <span data-ttu-id="2474e-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2474e-121">-Confirm</span></span>
<span data-ttu-id="2474e-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2474e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2474e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2474e-123">-WhatIf</span></span>
<span data-ttu-id="2474e-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2474e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2474e-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2474e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2474e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2474e-126">-DefaultProfile</span></span>
<span data-ttu-id="2474e-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2474e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2474e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2474e-128">CommonParameters</span></span>
<span data-ttu-id="2474e-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2474e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2474e-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2474e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2474e-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2474e-131">INPUTS</span></span>

## <span data-ttu-id="2474e-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2474e-132">OUTPUTS</span></span>

### <span data-ttu-id="2474e-133">Microsoft. Azure. Commands. SQL. Security. model. DatabaseSecureConnectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="2474e-133">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="2474e-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2474e-134">NOTES</span></span>

## <span data-ttu-id="2474e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2474e-135">RELATED LINKS</span></span>

