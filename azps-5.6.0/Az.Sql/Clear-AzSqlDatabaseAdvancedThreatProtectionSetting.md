---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8c9f8bfad95a7bbefd6e685701813d0c383f2b8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979226"
---
# <span data-ttu-id="78866-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="78866-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="78866-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78866-102">SYNOPSIS</span></span>
<span data-ttu-id="78866-103">Usuwa z bazy danych zaawansowane ustawienia ochrony przed zagrożeniami.</span><span class="sxs-lookup"><span data-stu-id="78866-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="78866-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="78866-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78866-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="78866-105">DESCRIPTION</span></span>
<span data-ttu-id="78866-106">Polecenie cmdlet **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** usuwa zaawansowane ustawienia ochrony przed zagrożeniami z bazy danych AzureAzure SQL.</span><span class="sxs-lookup"><span data-stu-id="78866-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="78866-107">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* i *ServerName* w celu zidentyfikowania bazy danych, z której to polecenie cmdlet usuwa ustawienia.</span><span class="sxs-lookup"><span data-stu-id="78866-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="78866-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="78866-108">EXAMPLES</span></span>

### <span data-ttu-id="78866-109">Przykład 1. Usuwanie zaawansowanych ustawień ochrony przed zagrożeniami dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="78866-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="78866-110">To polecenie usuwa zaawansowane ustawienia ochrony przed zagrożeniami z bazy danych o nazwie Database01 na serwerze o nazwie Serwer01.</span><span class="sxs-lookup"><span data-stu-id="78866-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="78866-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78866-111">PARAMETERS</span></span>

### <span data-ttu-id="78866-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="78866-112">-DatabaseName</span></span>
<span data-ttu-id="78866-113">Określa nazwę bazy danych, w której należy usunąć zaawansowane ustawienia ochrony przed zagrożeniami.</span><span class="sxs-lookup"><span data-stu-id="78866-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

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

### <span data-ttu-id="78866-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78866-114">-DefaultProfile</span></span>
<span data-ttu-id="78866-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="78866-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78866-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78866-116">-PassThru</span></span>
<span data-ttu-id="78866-117">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="78866-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="78866-118">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="78866-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="78866-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78866-119">-ResourceGroupName</span></span>
<span data-ttu-id="78866-120">Określa nazwę grupy zasobów, do której należy serwer.</span><span class="sxs-lookup"><span data-stu-id="78866-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="78866-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="78866-121">-ServerName</span></span>
<span data-ttu-id="78866-122">Określa nazwę serwera, na którym jest uruchomiona baza danych.</span><span class="sxs-lookup"><span data-stu-id="78866-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="78866-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="78866-123">-Confirm</span></span>
<span data-ttu-id="78866-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="78866-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78866-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78866-125">-WhatIf</span></span>
<span data-ttu-id="78866-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78866-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78866-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="78866-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78866-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78866-128">CommonParameters</span></span>
<span data-ttu-id="78866-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78866-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78866-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78866-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78866-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78866-131">INPUTS</span></span>

### <span data-ttu-id="78866-132">System.String</span><span class="sxs-lookup"><span data-stu-id="78866-132">System.String</span></span>

## <span data-ttu-id="78866-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78866-133">OUTPUTS</span></span>

### <span data-ttu-id="78866-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="78866-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="78866-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="78866-135">NOTES</span></span>

## <span data-ttu-id="78866-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78866-136">RELATED LINKS</span></span>

[<span data-ttu-id="78866-137">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="78866-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


