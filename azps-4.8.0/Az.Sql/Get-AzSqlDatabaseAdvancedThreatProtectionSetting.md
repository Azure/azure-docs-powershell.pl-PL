---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 9035f2a03ac04a9bc99248c48675ab3c69b84207
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415363"
---
# <span data-ttu-id="5661f-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="5661f-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="5661f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5661f-102">SYNOPSIS</span></span>
<span data-ttu-id="5661f-103">Pobiera zaawansowane ustawienia ochrony przed zagrożeniami dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5661f-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="5661f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5661f-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSetting [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5661f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5661f-105">DESCRIPTION</span></span>
<span data-ttu-id="5661f-106">Polecenie **cmdlet Get-AzSqlDatabaseAdvancedThreatProtectionSetting** pobiera zaawansowane ustawienia ochrony przed zagrożeniami w bazie danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="5661f-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="5661f-107">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName*, *ServerName* i *DatabaseName* w celu określenia bazy danych, dla której to polecenie cmdlet uzyskuje ustawienia.</span><span class="sxs-lookup"><span data-stu-id="5661f-107">To use this cmdlet, specify the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="5661f-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5661f-108">EXAMPLES</span></span>

### <span data-ttu-id="5661f-109">Przykład 1. Uzyskiwanie zaawansowanych ustawień ochrony przed zagrożeniami dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="5661f-109">Example 1: Get the advanced threat protection settings for a database</span></span>
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

<span data-ttu-id="5661f-110">To polecenie pobiera zaawansowane ustawienia ochrony przed zagrożeniami dla bazy danych o nazwie Database01.</span><span class="sxs-lookup"><span data-stu-id="5661f-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="5661f-111">Baza danych znajduje się na serwerze o nazwie Server01, który jest przypisany do grupy zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5661f-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="5661f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5661f-112">PARAMETERS</span></span>

### <span data-ttu-id="5661f-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5661f-113">-DatabaseName</span></span>
<span data-ttu-id="5661f-114">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5661f-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="5661f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5661f-115">-DefaultProfile</span></span>
<span data-ttu-id="5661f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="5661f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5661f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5661f-117">-ResourceGroupName</span></span>
<span data-ttu-id="5661f-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="5661f-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5661f-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5661f-119">-ServerName</span></span>
<span data-ttu-id="5661f-120">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="5661f-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="5661f-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5661f-121">-Confirm</span></span>
<span data-ttu-id="5661f-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5661f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5661f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5661f-123">-WhatIf</span></span>
<span data-ttu-id="5661f-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5661f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5661f-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5661f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5661f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5661f-126">CommonParameters</span></span>
<span data-ttu-id="5661f-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5661f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5661f-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5661f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5661f-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5661f-129">INPUTS</span></span>

### <span data-ttu-id="5661f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5661f-130">System.String</span></span>

## <span data-ttu-id="5661f-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5661f-131">OUTPUTS</span></span>

### <span data-ttu-id="5661f-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="5661f-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="5661f-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5661f-133">NOTES</span></span>

## <span data-ttu-id="5661f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5661f-134">RELATED LINKS</span></span>




