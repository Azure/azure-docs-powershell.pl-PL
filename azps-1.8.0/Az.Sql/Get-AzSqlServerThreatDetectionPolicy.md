---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: f8d01165825c63ece34779f58cb94a3f8e0af40c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707898"
---
# <span data-ttu-id="48966-101">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="48966-101">Get-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="48966-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48966-102">SYNOPSIS</span></span>
<span data-ttu-id="48966-103">Pobiera zasady wykrywania zagrożeń dla serwera.</span><span class="sxs-lookup"><span data-stu-id="48966-103">Gets the threat detection policy for a server.</span></span>

## <span data-ttu-id="48966-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48966-104">SYNTAX</span></span>

```
Get-AzSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48966-105">Opis</span><span class="sxs-lookup"><span data-stu-id="48966-105">DESCRIPTION</span></span>
<span data-ttu-id="48966-106">Polecenie cmdlet **Get-AzSqlServerThreatDetectionPolicy** pobiera zasady wykrywania zagrożeń na platformie Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="48966-106">The **Get-AzSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="48966-107">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* oraz *nazwa_serwera* w celu zidentyfikowania serwera, dla którego to polecenie cmdlet będzie pobierać zasady.</span><span class="sxs-lookup"><span data-stu-id="48966-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="48966-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48966-108">EXAMPLES</span></span>

### <span data-ttu-id="48966-109">Przykład 1: uzyskiwanie zasad wykrywania zagrożeń dla serwera</span><span class="sxs-lookup"><span data-stu-id="48966-109">Example 1: Get the threat detection policy for a server</span></span>
```
PS C:\>Get-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="48966-110">To polecenie pobiera zasady wykrywania zagrożeń dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="48966-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="48966-111">Serwer jest przypisany do grupy zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="48966-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="48966-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48966-112">PARAMETERS</span></span>

### <span data-ttu-id="48966-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48966-113">-DefaultProfile</span></span>
<span data-ttu-id="48966-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="48966-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48966-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48966-115">-ResourceGroupName</span></span>
<span data-ttu-id="48966-116">Określa nazwę grupy zasobów, do której należy serwer.</span><span class="sxs-lookup"><span data-stu-id="48966-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="48966-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="48966-117">-ServerName</span></span>
<span data-ttu-id="48966-118">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="48966-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="48966-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48966-119">-Confirm</span></span>
<span data-ttu-id="48966-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48966-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48966-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48966-121">-WhatIf</span></span>
<span data-ttu-id="48966-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48966-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48966-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="48966-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48966-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48966-124">CommonParameters</span></span>
<span data-ttu-id="48966-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48966-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48966-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48966-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48966-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48966-127">INPUTS</span></span>

### <span data-ttu-id="48966-128">System. String</span><span class="sxs-lookup"><span data-stu-id="48966-128">System.String</span></span>

## <span data-ttu-id="48966-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48966-129">OUTPUTS</span></span>

### <span data-ttu-id="48966-130">Microsoft. Azure. Commands. SQL. ThreatDetection. model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="48966-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="48966-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48966-131">NOTES</span></span>

## <span data-ttu-id="48966-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48966-132">RELATED LINKS</span></span>

[<span data-ttu-id="48966-133">Remove-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="48966-133">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="48966-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="48966-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


