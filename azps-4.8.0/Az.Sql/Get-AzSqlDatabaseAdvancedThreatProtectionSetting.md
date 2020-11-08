---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8090ee9cf6ec251668dbeadba6b18a7cde4898c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222232"
---
# <span data-ttu-id="05dbd-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="05dbd-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="05dbd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="05dbd-103">Pobiera zaawansowane ustawienia ochrony przed zagrożeniami dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="05dbd-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="05dbd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05dbd-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSetting [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05dbd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="05dbd-105">DESCRIPTION</span></span>
<span data-ttu-id="05dbd-106">Polecenie cmdlet **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** pobiera zaawansowane ustawienia ochrony przed zagrożeniami bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="05dbd-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="05dbd-107">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych, dla której to polecenie cmdlet uzyska ustawienia.</span><span class="sxs-lookup"><span data-stu-id="05dbd-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="05dbd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05dbd-108">EXAMPLES</span></span>

### <span data-ttu-id="05dbd-109">Przykład 1: uzyskiwanie zaawansowanych ustawień ochrony przed zagrożeniami dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="05dbd-109">Example 1: Get the advanced threat protection settings for a database</span></span>
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

<span data-ttu-id="05dbd-110">To polecenie pobiera zaawansowane ustawienia ochrony przed zagrożeniami dla bazy danych o nazwie Database01.</span><span class="sxs-lookup"><span data-stu-id="05dbd-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="05dbd-111">Baza danych znajduje się na serwerze o nazwie Server01, który jest przypisany do ResourceGroup11 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="05dbd-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="05dbd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05dbd-112">PARAMETERS</span></span>

### <span data-ttu-id="05dbd-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="05dbd-113">-DatabaseName</span></span>
<span data-ttu-id="05dbd-114">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="05dbd-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="05dbd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05dbd-115">-DefaultProfile</span></span>
<span data-ttu-id="05dbd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="05dbd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05dbd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05dbd-117">-ResourceGroupName</span></span>
<span data-ttu-id="05dbd-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="05dbd-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="05dbd-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="05dbd-119">-ServerName</span></span>
<span data-ttu-id="05dbd-120">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="05dbd-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="05dbd-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05dbd-121">-Confirm</span></span>
<span data-ttu-id="05dbd-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05dbd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05dbd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05dbd-123">-WhatIf</span></span>
<span data-ttu-id="05dbd-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05dbd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05dbd-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="05dbd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05dbd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05dbd-126">CommonParameters</span></span>
<span data-ttu-id="05dbd-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05dbd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05dbd-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05dbd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05dbd-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05dbd-129">INPUTS</span></span>

### <span data-ttu-id="05dbd-130">System. String</span><span class="sxs-lookup"><span data-stu-id="05dbd-130">System.String</span></span>

## <span data-ttu-id="05dbd-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05dbd-131">OUTPUTS</span></span>

### <span data-ttu-id="05dbd-132">Microsoft. Azure. Commands. SQL. ThreatDetection. model. DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="05dbd-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="05dbd-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05dbd-133">NOTES</span></span>

## <span data-ttu-id="05dbd-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05dbd-134">RELATED LINKS</span></span>

[<span data-ttu-id="05dbd-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="05dbd-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)



