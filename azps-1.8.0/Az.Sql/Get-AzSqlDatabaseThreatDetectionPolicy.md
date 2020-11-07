---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 6cb14b368bf7f190c30ff32fdec12576d3189204
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707977"
---
# <span data-ttu-id="5c4c5-101">Get-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c4c5-101">Get-AzSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="5c4c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c4c5-102">SYNOPSIS</span></span>
<span data-ttu-id="5c4c5-103">Pobiera zasady wykrywania zagrożeń dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-103">Gets the threat detection policy for a database.</span></span>

## <span data-ttu-id="5c4c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c4c5-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseThreatDetectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c4c5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5c4c5-105">DESCRIPTION</span></span>
<span data-ttu-id="5c4c5-106">Polecenie cmdlet **Get-AzSqlDatabaseThreatDetectionPolicy** pobiera zasady wykrywania zagrożeń dla bazy danych usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-106">The **Get-AzSqlDatabaseThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL database.</span></span>
<span data-ttu-id="5c4c5-107">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych, dla której to polecenie cmdlet ma pobierać zasady.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="5c4c5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c4c5-108">EXAMPLES</span></span>

### <span data-ttu-id="5c4c5-109">Przykład 1: uzyskiwanie zasad wykrywania zagrożeń dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="5c4c5-109">Example 1: Get the threat detection policy for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="5c4c5-110">To polecenie pobiera zasady wykrywania zagrożeń dla bazy danych o nazwie Database01.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-110">This command gets the threat detection policy for a database named Database01.</span></span>
<span data-ttu-id="5c4c5-111">Baza danych znajduje się na serwerze o nazwie Server01, który jest przypisany do ResourceGroup11 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="5c4c5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c4c5-112">PARAMETERS</span></span>

### <span data-ttu-id="5c4c5-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c4c5-113">-DatabaseName</span></span>
<span data-ttu-id="5c4c5-114">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="5c4c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c4c5-115">-DefaultProfile</span></span>
<span data-ttu-id="5c4c5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5c4c5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c4c5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c4c5-117">-ResourceGroupName</span></span>
<span data-ttu-id="5c4c5-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5c4c5-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="5c4c5-119">-ServerName</span></span>
<span data-ttu-id="5c4c5-120">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="5c4c5-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5c4c5-121">-Confirm</span></span>
<span data-ttu-id="5c4c5-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c4c5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c4c5-123">-WhatIf</span></span>
<span data-ttu-id="5c4c5-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c4c5-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c4c5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c4c5-126">CommonParameters</span></span>
<span data-ttu-id="5c4c5-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c4c5-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c4c5-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c4c5-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c4c5-129">INPUTS</span></span>

### <span data-ttu-id="5c4c5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5c4c5-130">System.String</span></span>

## <span data-ttu-id="5c4c5-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c4c5-131">OUTPUTS</span></span>

### <span data-ttu-id="5c4c5-132">Microsoft. Azure. Commands. SQL. ThreatDetection. model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5c4c5-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="5c4c5-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c4c5-133">NOTES</span></span>

## <span data-ttu-id="5c4c5-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c4c5-134">RELATED LINKS</span></span>

[<span data-ttu-id="5c4c5-135">Remove-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c4c5-135">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzSqlDatabaseThreatDetectionPolicy.md)



