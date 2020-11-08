---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8ff7e7df12bc1415cfe6e4b14dc673e93d8d8791
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063173"
---
# <span data-ttu-id="3896a-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="3896a-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="3896a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3896a-102">SYNOPSIS</span></span>
<span data-ttu-id="3896a-103">Usuwa zaawansowane ustawienia ochrony przed zagrożeniami z serwera.</span><span class="sxs-lookup"><span data-stu-id="3896a-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="3896a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3896a-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3896a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3896a-105">DESCRIPTION</span></span>
<span data-ttu-id="3896a-106">Polecenie cmdlet Clear-AzSqlServerAdvancedThreatProtectionSetting usuwa ustawienia zaawansowanego zabezpieczenia przed zagrożeniami z programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3896a-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="3896a-107">Aby użyć tego polecenia cmdlet, określ parametry ResourceGroupName oraz nazwa_serwera w celu zidentyfikowania serwera, z którego to polecenie cmdlet usunie ustawienia.</span><span class="sxs-lookup"><span data-stu-id="3896a-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="3896a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3896a-108">EXAMPLES</span></span>

### <span data-ttu-id="3896a-109">Przykład 1: usuwanie zaawansowanych ustawień ochrony przed zagrożeniami dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="3896a-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="3896a-110">To polecenie usuwa zaawansowane ustawienia ochrony przed zagrożeniami z serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="3896a-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="3896a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3896a-111">PARAMETERS</span></span>

### <span data-ttu-id="3896a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3896a-112">-DefaultProfile</span></span>
<span data-ttu-id="3896a-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3896a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3896a-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3896a-114">-PassThru</span></span>
<span data-ttu-id="3896a-115">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="3896a-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3896a-116">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3896a-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3896a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3896a-117">-ResourceGroupName</span></span>
<span data-ttu-id="3896a-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="3896a-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="3896a-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="3896a-119">-ServerName</span></span>
<span data-ttu-id="3896a-120">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="3896a-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="3896a-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3896a-121">-Confirm</span></span>
<span data-ttu-id="3896a-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3896a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3896a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3896a-123">-WhatIf</span></span>
<span data-ttu-id="3896a-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3896a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3896a-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3896a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3896a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3896a-126">CommonParameters</span></span>
<span data-ttu-id="3896a-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3896a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3896a-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3896a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3896a-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3896a-129">INPUTS</span></span>

### <span data-ttu-id="3896a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3896a-130">System.String</span></span>

## <span data-ttu-id="3896a-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3896a-131">OUTPUTS</span></span>

### <span data-ttu-id="3896a-132">Microsoft. Azure. Commands. SQL. ThreatDetection. model. ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="3896a-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="3896a-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3896a-133">NOTES</span></span>

## <span data-ttu-id="3896a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3896a-134">RELATED LINKS</span></span>

[<span data-ttu-id="3896a-135">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="3896a-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

