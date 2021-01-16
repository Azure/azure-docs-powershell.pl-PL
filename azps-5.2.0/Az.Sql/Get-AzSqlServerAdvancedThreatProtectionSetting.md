---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 94963c8c5d61c91e2d53cdf7b12cc333acc566a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333277"
---
# <span data-ttu-id="22e24-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="22e24-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="22e24-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22e24-102">SYNOPSIS</span></span>
<span data-ttu-id="22e24-103">Pobiera zaawansowane ustawienia ochrony przed zagrożeniami dla serwera.</span><span class="sxs-lookup"><span data-stu-id="22e24-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="22e24-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22e24-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSetting -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22e24-105">Opis</span><span class="sxs-lookup"><span data-stu-id="22e24-105">DESCRIPTION</span></span>
<span data-ttu-id="22e24-106">Polecenie cmdlet **Get-AzSqlServerAdvancedThreatProtectionSetting** pobiera zaawansowane ustawienia ochrony przed zagrożeniami dotyczące programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="22e24-106">The **Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="22e24-107">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* oraz *nazwa_serwera* w celu zidentyfikowania serwera, dla którego to polecenie cmdlet uzyska ustawienia.</span><span class="sxs-lookup"><span data-stu-id="22e24-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="22e24-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22e24-108">EXAMPLES</span></span>

### <span data-ttu-id="22e24-109">Przykład 1: uzyskiwanie zaawansowanych ustawień ochrony przed zagrożeniami dla serwera</span><span class="sxs-lookup"><span data-stu-id="22e24-109">Example 1: Get the advanced threat protection settings for a server</span></span>
```
PS C:\>Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="22e24-110">To polecenie pobiera zaawansowane ustawienia ochrony przed zagrożeniami dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="22e24-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="22e24-111">Serwer jest przypisany do grupy zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="22e24-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="22e24-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22e24-112">PARAMETERS</span></span>

### <span data-ttu-id="22e24-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e24-113">-DefaultProfile</span></span>
<span data-ttu-id="22e24-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="22e24-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22e24-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22e24-115">-ResourceGroupName</span></span>
<span data-ttu-id="22e24-116">Określa nazwę grupy zasobów, do której należy serwer.</span><span class="sxs-lookup"><span data-stu-id="22e24-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="22e24-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="22e24-117">-ServerName</span></span>
<span data-ttu-id="22e24-118">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="22e24-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="22e24-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="22e24-119">-Confirm</span></span>
<span data-ttu-id="22e24-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22e24-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22e24-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22e24-121">-WhatIf</span></span>
<span data-ttu-id="22e24-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22e24-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22e24-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="22e24-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22e24-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e24-124">CommonParameters</span></span>
<span data-ttu-id="22e24-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22e24-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e24-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22e24-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e24-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22e24-127">INPUTS</span></span>

### <span data-ttu-id="22e24-128">System. String</span><span class="sxs-lookup"><span data-stu-id="22e24-128">System.String</span></span>

## <span data-ttu-id="22e24-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22e24-129">OUTPUTS</span></span>

### <span data-ttu-id="22e24-130">Microsoft. Azure. Commands. SQL. ThreatDetection. model. ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="22e24-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="22e24-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22e24-131">NOTES</span></span>

## <span data-ttu-id="22e24-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22e24-132">RELATED LINKS</span></span>

[<span data-ttu-id="22e24-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="22e24-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)

[<span data-ttu-id="22e24-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="22e24-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


