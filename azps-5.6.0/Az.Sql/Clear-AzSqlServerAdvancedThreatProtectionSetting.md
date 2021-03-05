---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4a576c930d8ff1c53c6c9e92c7d87664aef4da4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011601"
---
# <span data-ttu-id="f453b-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="f453b-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="f453b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f453b-102">SYNOPSIS</span></span>
<span data-ttu-id="f453b-103">Usuwa z serwera zaawansowane ustawienia ochrony przed zagrożeniami.</span><span class="sxs-lookup"><span data-stu-id="f453b-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="f453b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f453b-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f453b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f453b-105">DESCRIPTION</span></span>
<span data-ttu-id="f453b-106">Polecenie Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet usuwa zaawansowane ustawienia ochrony przed zagrożeniami z serwera Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f453b-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="f453b-107">Aby użyć tego polecenia cmdlet, określ parametry ResourceGroupName i ServerName w celu określenia serwera, z którego to polecenie cmdlet usuwa ustawienia.</span><span class="sxs-lookup"><span data-stu-id="f453b-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="f453b-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f453b-108">EXAMPLES</span></span>

### <span data-ttu-id="f453b-109">Przykład 1. Usuwanie zaawansowanych ustawień ochrony przed zagrożeniami dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="f453b-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="f453b-110">To polecenie usuwa zaawansowane ustawienia ochrony przed zagrożeniami z serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="f453b-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="f453b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f453b-111">PARAMETERS</span></span>

### <span data-ttu-id="f453b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f453b-112">-DefaultProfile</span></span>
<span data-ttu-id="f453b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f453b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f453b-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f453b-114">-PassThru</span></span>
<span data-ttu-id="f453b-115">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="f453b-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f453b-116">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f453b-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f453b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f453b-117">-ResourceGroupName</span></span>
<span data-ttu-id="f453b-118">Określa nazwę grupy zasobów, do których jest przydzielony serwer.</span><span class="sxs-lookup"><span data-stu-id="f453b-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="f453b-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f453b-119">-ServerName</span></span>
<span data-ttu-id="f453b-120">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="f453b-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="f453b-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f453b-121">-Confirm</span></span>
<span data-ttu-id="f453b-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f453b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f453b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f453b-123">-WhatIf</span></span>
<span data-ttu-id="f453b-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f453b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f453b-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f453b-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f453b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f453b-126">CommonParameters</span></span>
<span data-ttu-id="f453b-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f453b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f453b-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f453b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f453b-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f453b-129">INPUTS</span></span>

### <span data-ttu-id="f453b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f453b-130">System.String</span></span>

## <span data-ttu-id="f453b-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f453b-131">OUTPUTS</span></span>

### <span data-ttu-id="f453b-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="f453b-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="f453b-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f453b-133">NOTES</span></span>

## <span data-ttu-id="f453b-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f453b-134">RELATED LINKS</span></span>

[<span data-ttu-id="f453b-135">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="f453b-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

