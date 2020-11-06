---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: d6e9ac96a5263add451fb03eae7783fe344852fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526017"
---
# <span data-ttu-id="722fc-101">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="722fc-101">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="722fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="722fc-102">SYNOPSIS</span></span>
<span data-ttu-id="722fc-103">Pobiera zasady wykrywania zagrożeń dla serwera.</span><span class="sxs-lookup"><span data-stu-id="722fc-103">Gets the threat detection policy for a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="722fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="722fc-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="722fc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="722fc-105">DESCRIPTION</span></span>
<span data-ttu-id="722fc-106">Polecenie cmdlet **Get-AzureRmSqlServerThreatDetectionPolicy** pobiera zasady wykrywania zagrożeń na platformie Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="722fc-106">The **Get-AzureRmSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="722fc-107">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* oraz *nazwa_serwera* w celu zidentyfikowania serwera, dla którego to polecenie cmdlet będzie pobierać zasady.</span><span class="sxs-lookup"><span data-stu-id="722fc-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="722fc-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="722fc-108">EXAMPLES</span></span>

### <span data-ttu-id="722fc-109">Przykład 1: uzyskiwanie zasad wykrywania zagrożeń dla serwera</span><span class="sxs-lookup"><span data-stu-id="722fc-109">Example 1: Get the threat detection policy for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="722fc-110">To polecenie pobiera zasady wykrywania zagrożeń dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="722fc-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="722fc-111">Serwer jest przypisany do grupy zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="722fc-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="722fc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="722fc-112">PARAMETERS</span></span>

### <span data-ttu-id="722fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="722fc-113">-DefaultProfile</span></span>
<span data-ttu-id="722fc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="722fc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="722fc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="722fc-115">-ResourceGroupName</span></span>
<span data-ttu-id="722fc-116">Określa nazwę grupy zasobów, do której należy serwer.</span><span class="sxs-lookup"><span data-stu-id="722fc-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="722fc-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="722fc-117">-ServerName</span></span>
<span data-ttu-id="722fc-118">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="722fc-118">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="722fc-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="722fc-119">-Confirm</span></span>
<span data-ttu-id="722fc-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="722fc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="722fc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="722fc-121">-WhatIf</span></span>
<span data-ttu-id="722fc-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="722fc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="722fc-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="722fc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="722fc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="722fc-124">CommonParameters</span></span>
<span data-ttu-id="722fc-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="722fc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="722fc-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="722fc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="722fc-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="722fc-127">INPUTS</span></span>

### <span data-ttu-id="722fc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="722fc-128">System.String</span></span>

## <span data-ttu-id="722fc-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="722fc-129">OUTPUTS</span></span>

### <span data-ttu-id="722fc-130">Microsoft. Azure. Commands. SQL. ThreatDetection. model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="722fc-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="722fc-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="722fc-131">NOTES</span></span>

## <span data-ttu-id="722fc-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="722fc-132">RELATED LINKS</span></span>

[<span data-ttu-id="722fc-133">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="722fc-133">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="722fc-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="722fc-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


