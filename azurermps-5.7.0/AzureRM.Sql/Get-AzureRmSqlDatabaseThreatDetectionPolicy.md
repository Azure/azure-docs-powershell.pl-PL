---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: ad07f080b659ff03c96f806ad7b69446c4491fb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547924"
---
# <span data-ttu-id="c8373-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c8373-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="c8373-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8373-102">SYNOPSIS</span></span>
<span data-ttu-id="c8373-103">Pobiera zasady wykrywania zagrożeń dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c8373-103">Gets the threat detection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8373-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8373-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseThreatDetectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8373-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c8373-105">DESCRIPTION</span></span>
<span data-ttu-id="c8373-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseThreatDetectionPolicy** pobiera zasady wykrywania zagrożeń dla bazy danych usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c8373-106">The **Get-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL database.</span></span>
<span data-ttu-id="c8373-107">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych, dla której to polecenie cmdlet ma pobierać zasady.</span><span class="sxs-lookup"><span data-stu-id="c8373-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="c8373-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8373-108">EXAMPLES</span></span>

### <span data-ttu-id="c8373-109">Przykład 1: uzyskiwanie zasad wykrywania zagrożeń dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="c8373-109">Example 1: Get the threat detection policy for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="c8373-110">To polecenie pobiera zasady wykrywania zagrożeń dla bazy danych o nazwie Database01.</span><span class="sxs-lookup"><span data-stu-id="c8373-110">This command gets the threat detection policy for a database named Database01.</span></span>
<span data-ttu-id="c8373-111">Baza danych znajduje się na serwerze o nazwie Server01, który jest przypisany do ResourceGroup11 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c8373-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="c8373-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8373-112">PARAMETERS</span></span>

### <span data-ttu-id="c8373-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c8373-113">-DatabaseName</span></span>
<span data-ttu-id="c8373-114">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c8373-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="c8373-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8373-115">-DefaultProfile</span></span>
<span data-ttu-id="c8373-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c8373-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8373-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8373-117">-ResourceGroupName</span></span>
<span data-ttu-id="c8373-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="c8373-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c8373-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c8373-119">-ServerName</span></span>
<span data-ttu-id="c8373-120">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="c8373-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="c8373-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c8373-121">-Confirm</span></span>
<span data-ttu-id="c8373-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8373-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8373-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8373-123">-WhatIf</span></span>
<span data-ttu-id="c8373-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8373-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8373-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c8373-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8373-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8373-126">CommonParameters</span></span>
<span data-ttu-id="c8373-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8373-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8373-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8373-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8373-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8373-129">INPUTS</span></span>

###  
<span data-ttu-id="c8373-130">Nie możesz popotokować danych wejściowych tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8373-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="c8373-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8373-131">OUTPUTS</span></span>

### <span data-ttu-id="c8373-132">Microsoft. Azure. Commands. SQL. ThreatDetection. model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c8373-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="c8373-133">To polecenie cmdlet zwraca obiekt **model. DatabaseThreatDetectionPolicyModel** .</span><span class="sxs-lookup"><span data-stu-id="c8373-133">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="c8373-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8373-134">NOTES</span></span>

## <span data-ttu-id="c8373-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8373-135">RELATED LINKS</span></span>

[<span data-ttu-id="c8373-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c8373-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)



