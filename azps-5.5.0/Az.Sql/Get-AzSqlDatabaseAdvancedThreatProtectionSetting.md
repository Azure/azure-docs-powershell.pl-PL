---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8090ee9cf6ec251668dbeadba6b18a7cde4898c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176994"
---
# <span data-ttu-id="2de2b-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="2de2b-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="2de2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2de2b-102">SYNOPSIS</span></span>
<span data-ttu-id="2de2b-103">Pobiera zaawansowane ustawienia ochrony przed zagrożeniami dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2de2b-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="2de2b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2de2b-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSetting [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2de2b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2de2b-105">DESCRIPTION</span></span>
<span data-ttu-id="2de2b-106">Polecenie **cmdlet Get-AzSqlDatabaseAdvancedThreatProtectionSetting** pobiera zaawansowane ustawienia ochrony przed zagrożeniami w bazie danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2de2b-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="2de2b-107">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName*, *ServerName* i *DatabaseName* w celu określenia bazy danych, dla której to polecenie cmdlet uzyskuje ustawienia.</span><span class="sxs-lookup"><span data-stu-id="2de2b-107">To use this cmdlet, specify the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="2de2b-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2de2b-108">EXAMPLES</span></span>

### <span data-ttu-id="2de2b-109">Przykład 1. Uzyskiwanie zaawansowanych ustawień ochrony przed zagrożeniami dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="2de2b-109">Example 1: Get the advanced threat protection settings for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="2de2b-110">To polecenie pobiera zaawansowane ustawienia ochrony przed zagrożeniami dla bazy danych o nazwie Database01.</span><span class="sxs-lookup"><span data-stu-id="2de2b-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="2de2b-111">Baza danych znajduje się na serwerze o nazwie Server01, który jest przypisany do grupy zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2de2b-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="2de2b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2de2b-112">PARAMETERS</span></span>

### <span data-ttu-id="2de2b-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2de2b-113">-DatabaseName</span></span>
<span data-ttu-id="2de2b-114">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2de2b-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="2de2b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de2b-115">-DefaultProfile</span></span>
<span data-ttu-id="2de2b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="2de2b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2de2b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de2b-117">-ResourceGroupName</span></span>
<span data-ttu-id="2de2b-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="2de2b-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="2de2b-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2de2b-119">-ServerName</span></span>
<span data-ttu-id="2de2b-120">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="2de2b-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="2de2b-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2de2b-121">-Confirm</span></span>
<span data-ttu-id="2de2b-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2de2b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2de2b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2de2b-123">-WhatIf</span></span>
<span data-ttu-id="2de2b-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2de2b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2de2b-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2de2b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2de2b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de2b-126">CommonParameters</span></span>
<span data-ttu-id="2de2b-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2de2b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de2b-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2de2b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de2b-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2de2b-129">INPUTS</span></span>

### <span data-ttu-id="2de2b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2de2b-130">System.String</span></span>

## <span data-ttu-id="2de2b-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2de2b-131">OUTPUTS</span></span>

### <span data-ttu-id="2de2b-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="2de2b-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="2de2b-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2de2b-133">NOTES</span></span>

## <span data-ttu-id="2de2b-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2de2b-134">RELATED LINKS</span></span>

[<span data-ttu-id="2de2b-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="2de2b-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)



