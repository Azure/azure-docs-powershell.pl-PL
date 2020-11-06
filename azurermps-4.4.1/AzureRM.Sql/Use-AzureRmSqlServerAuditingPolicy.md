---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 9e3e94109904bc14f22e2ca2c08936316ed597db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549084"
---
# <span data-ttu-id="e608c-101">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="e608c-101">Use-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="e608c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e608c-102">SYNOPSIS</span></span>
<span data-ttu-id="e608c-103">Określa, że baza danych używa zasad inspekcji swojego serwera hosta.</span><span class="sxs-lookup"><span data-stu-id="e608c-103">Specifies that a database uses the auditing policy of its host server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e608c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e608c-104">SYNTAX</span></span>

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e608c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e608c-105">DESCRIPTION</span></span>
<span data-ttu-id="e608c-106">Polecenie cmdlet **use-AzureRmSqlServerAuditingPolicy** określa, że baza danych używa zasad inspekcji serwera hosta.</span><span class="sxs-lookup"><span data-stu-id="e608c-106">The **Use-AzureRmSqlServerAuditingPolicy** cmdlet specifies that a database uses the auditing policy of its host server.</span></span>
<span data-ttu-id="e608c-107">Określ parametry *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* , które identyfikują bazę danych.</span><span class="sxs-lookup"><span data-stu-id="e608c-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="e608c-108">Jeśli dla serwera bazy danych nie zdefiniowano zasad inspekcji, to polecenie cmdlet nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="e608c-108">If no auditing policy is defined for the database server, this cmdlet fails.</span></span>

<span data-ttu-id="e608c-109">Jeśli host używa inspekcji na poziomie serwera, wykrywanie zagrożeń jest usuwane.</span><span class="sxs-lookup"><span data-stu-id="e608c-109">If the host uses server level auditing, threat detection is removed.</span></span>

## <span data-ttu-id="e608c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e608c-110">EXAMPLES</span></span>

### <span data-ttu-id="e608c-111">Przykład 1: Konfigurowanie bazy danych do korzystania z zasad inspekcji serwera</span><span class="sxs-lookup"><span data-stu-id="e608c-111">Example 1: Configure a database to use the auditing policy of its server</span></span>
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

<span data-ttu-id="e608c-112">To polecenie określa, że baza danych o nazwie Database01 na Server02 korzysta z zasad inspekcji serwera.</span><span class="sxs-lookup"><span data-stu-id="e608c-112">This command specifies that the database named Database01 on Server02 uses the auditing policy of the server.</span></span>

## <span data-ttu-id="e608c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e608c-113">PARAMETERS</span></span>

### <span data-ttu-id="e608c-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e608c-114">-DatabaseName</span></span>
<span data-ttu-id="e608c-115">Określa nazwę bazy danych, która będzie korzystać z zasad inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e608c-115">Specifies the name of the database that will use the auditing policy.</span></span>

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

### <span data-ttu-id="e608c-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e608c-116">-PassThru</span></span>
<span data-ttu-id="e608c-117">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e608c-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e608c-118">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e608c-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e608c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e608c-119">-ResourceGroupName</span></span>
<span data-ttu-id="e608c-120">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="e608c-120">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e608c-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="e608c-121">-ServerName</span></span>
<span data-ttu-id="e608c-122">Określa nazwę serwera obsługującego bazę danych, która używa zasad inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e608c-122">Specifies the name of the server that hosts the database that uses the auditing policy.</span></span>

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

### <span data-ttu-id="e608c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e608c-123">-DefaultProfile</span></span>
<span data-ttu-id="e608c-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e608c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e608c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e608c-125">CommonParameters</span></span>
<span data-ttu-id="e608c-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e608c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e608c-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e608c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e608c-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e608c-128">INPUTS</span></span>

## <span data-ttu-id="e608c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e608c-129">OUTPUTS</span></span>

### <span data-ttu-id="e608c-130">Microsoft. Azure. Commands. SQL. Security. model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e608c-130">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="e608c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e608c-131">NOTES</span></span>

## <span data-ttu-id="e608c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e608c-132">RELATED LINKS</span></span>

[<span data-ttu-id="e608c-133">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="e608c-133">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="e608c-134">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="e608c-134">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="e608c-135">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="e608c-135">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="e608c-136">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="e608c-136">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="e608c-137">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="e608c-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


