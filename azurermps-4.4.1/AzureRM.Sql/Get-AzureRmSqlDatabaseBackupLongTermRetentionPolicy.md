---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1C0AF5B2-7187-4BFA-8DBB-A771FD2E00A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: a4538210c95f8357a9b920f827e8812b47377a2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542863"
---
# <span data-ttu-id="fe085-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fe085-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="fe085-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe085-102">SYNOPSIS</span></span>
<span data-ttu-id="fe085-103">Pobiera zasady przechowywania długoterminowych baz danych.</span><span class="sxs-lookup"><span data-stu-id="fe085-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe085-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe085-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe085-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fe085-105">DESCRIPTION</span></span>
<span data-ttu-id="fe085-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** pobiera długoterminowe zasady przechowywania zarejestrowane w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="fe085-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="fe085-107">Zasady to zasób kopii zapasowej platformy Azure służący do definiowania zasad magazynu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="fe085-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="fe085-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe085-108">EXAMPLES</span></span>

## <span data-ttu-id="fe085-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe085-109">PARAMETERS</span></span>

### <span data-ttu-id="fe085-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fe085-110">-DatabaseName</span></span>
<span data-ttu-id="fe085-111">Określa nazwę bazy danych SQL, dla której to polecenie cmdlet pobiera zasady.</span><span class="sxs-lookup"><span data-stu-id="fe085-111">Specifies the name of the SQL Database for which this cmdlet gets a policy.</span></span>

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

### <span data-ttu-id="fe085-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe085-112">-ResourceGroupName</span></span>
<span data-ttu-id="fe085-113">Określa nazwę grupy zasobów zawierającej bazę danych.</span><span class="sxs-lookup"><span data-stu-id="fe085-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="fe085-114">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fe085-114">-ServerName</span></span>
<span data-ttu-id="fe085-115">Określa serwer, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="fe085-115">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="fe085-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fe085-116">-Confirm</span></span>
<span data-ttu-id="fe085-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe085-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe085-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe085-118">-WhatIf</span></span>
<span data-ttu-id="fe085-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe085-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe085-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fe085-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe085-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe085-121">-DefaultProfile</span></span>
<span data-ttu-id="fe085-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe085-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe085-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe085-123">CommonParameters</span></span>
<span data-ttu-id="fe085-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe085-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe085-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe085-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe085-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe085-126">INPUTS</span></span>

## <span data-ttu-id="fe085-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe085-127">OUTPUTS</span></span>

## <span data-ttu-id="fe085-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe085-128">NOTES</span></span>

## <span data-ttu-id="fe085-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe085-129">RELATED LINKS</span></span>

[<span data-ttu-id="fe085-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fe085-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="fe085-131">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="fe085-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
