---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 12cc605a95cb44b933c748156054135cb8395d61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547124"
---
# <span data-ttu-id="3b73b-101">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b73b-101">Import-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="3b73b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b73b-102">SYNOPSIS</span></span>
<span data-ttu-id="3b73b-103">Importuje konfigurację DSC do automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3b73b-103">Imports a DSC configuration into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b73b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b73b-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b73b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3b73b-105">DESCRIPTION</span></span>
<span data-ttu-id="3b73b-106">Polecenie cmdlet **Import-AzureRmAutomationDscConfiguration** importuje konfigurację konfiguracji pożądanego stanu (DSC) do usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3b73b-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="3b73b-107">Określ ścieżkę do skryptu APS, który zawiera jedną konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="3b73b-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="3b73b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b73b-108">EXAMPLES</span></span>

### <span data-ttu-id="3b73b-109">Przykład 1: Importowanie konfiguracji DSC do automatyzacji</span><span class="sxs-lookup"><span data-stu-id="3b73b-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="3b73b-110">To polecenie powoduje zaimportowanie konfiguracji DSC z pliku o nazwie client.ps1 do konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3b73b-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="3b73b-111">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="3b73b-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="3b73b-112">W przypadku istnienia istniejącej konfiguracji DSC to polecenie zastępuje je.</span><span class="sxs-lookup"><span data-stu-id="3b73b-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="3b73b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b73b-113">PARAMETERS</span></span>

### <span data-ttu-id="3b73b-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3b73b-114">-AutomationAccountName</span></span>
<span data-ttu-id="3b73b-115">Określa nazwę konta automatyzacji, do którego to polecenie cmdlet importuje konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="3b73b-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="3b73b-116">— Opis</span><span class="sxs-lookup"><span data-stu-id="3b73b-116">-Description</span></span>
<span data-ttu-id="3b73b-117">Określa opis konfiguracji zaimportowanej za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b73b-117">Specifies a description of the configuration that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b73b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3b73b-118">-Force</span></span>
<span data-ttu-id="3b73b-119">Wskazuje, że to polecenie cmdlet zastępuje istniejącą konfigurację DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3b73b-119">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="3b73b-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="3b73b-120">-LogVerbose</span></span>
<span data-ttu-id="3b73b-121">Określa, czy to polecenie cmdlet ma włączać i wyłączać pełne rejestrowanie w zadaniach kompilacji tej konfiguracji DSC.</span><span class="sxs-lookup"><span data-stu-id="3b73b-121">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="3b73b-122">Określ wartość $True, aby włączyć $False lub wyłączyć pełne logowanie w celu jego wyłączenia.</span><span class="sxs-lookup"><span data-stu-id="3b73b-122">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b73b-123">-Opublikowano</span><span class="sxs-lookup"><span data-stu-id="3b73b-123">-Published</span></span>
<span data-ttu-id="3b73b-124">Wskazuje, że to polecenie cmdlet zaimportuje konfigurację DSC w opublikowanym stanie.</span><span class="sxs-lookup"><span data-stu-id="3b73b-124">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="3b73b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b73b-125">-ResourceGroupName</span></span>
<span data-ttu-id="3b73b-126">Określa nazwę grupy zasobów, dla której to polecenie cmdlet zaimportuje konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="3b73b-126">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="3b73b-127">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="3b73b-127">-SourcePath</span></span>
<span data-ttu-id="3b73b-128">Określa ścieżkę wps_2 skryptu zawierającego konfigurację DSC zaimportowaną przez ten polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b73b-128">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b73b-129">-Tagi</span><span class="sxs-lookup"><span data-stu-id="3b73b-129">-Tags</span></span>
<span data-ttu-id="3b73b-130">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3b73b-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3b73b-131">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="3b73b-131">For example:</span></span>

<span data-ttu-id="3b73b-132">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="3b73b-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b73b-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b73b-133">-Confirm</span></span>
<span data-ttu-id="3b73b-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b73b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b73b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b73b-135">-WhatIf</span></span>
<span data-ttu-id="3b73b-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b73b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b73b-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3b73b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b73b-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b73b-138">-DefaultProfile</span></span>
<span data-ttu-id="3b73b-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b73b-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b73b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b73b-140">CommonParameters</span></span>
<span data-ttu-id="3b73b-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b73b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b73b-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b73b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b73b-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b73b-143">INPUTS</span></span>

## <span data-ttu-id="3b73b-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b73b-144">OUTPUTS</span></span>

### <span data-ttu-id="3b73b-145">Microsoft. Azure. Commands. Automation. model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b73b-145">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="3b73b-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b73b-146">NOTES</span></span>

## <span data-ttu-id="3b73b-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b73b-147">RELATED LINKS</span></span>

[<span data-ttu-id="3b73b-148">Eksportowanie — AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b73b-148">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="3b73b-149">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b73b-149">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)
