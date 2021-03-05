---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: e520fec3d0299ca2b5f74bb2a8a8b7de437d7a2a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008154"
---
# <span data-ttu-id="b8fd3-101">Get-AzAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="b8fd3-101">Get-AzAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="b8fd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="b8fd3-103">Tworzy pliki mof w konfiguracji meta.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-103">Creates meta-configuration .mof files.</span></span>

## <span data-ttu-id="b8fd3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b8fd3-104">SYNTAX</span></span>

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8fd3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b8fd3-105">DESCRIPTION</span></span>
<span data-ttu-id="b8fd3-106">Polecenie **cmdlet Get-AzAutomationDscOnboardingMetaconfig** tworzy pliki CMD (APS Desired State Configuration, DSC) meta-configuration Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b8fd3-106">The **Get-AzAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="b8fd3-107">To polecenie cmdlet tworzy plik mof dla każdej określonej nazwy komputera.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="b8fd3-108">Polecenie cmdlet tworzy folder na pliki mof.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="b8fd3-109">Możesz uruchomić polecenie cmdlet Set-DscLocalConfigurationManager tego folderu, aby dodać te komputery do konta usługi Azure Automation jako węzły DSC.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="b8fd3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b8fd3-110">EXAMPLES</span></span>

### <span data-ttu-id="b8fd3-111">Przykład 1. Dołączanie serwerów do automatyzacji dsc</span><span class="sxs-lookup"><span data-stu-id="b8fd3-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="b8fd3-112">Pierwsze polecenie tworzy pliki meta konfiguracji dsc dla dwóch serwerów dla konta automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="b8fd3-113">Polecenie zapisuje te pliki na pulpicie.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-113">The command saves these files on a desktop.</span></span>
<span data-ttu-id="b8fd3-114">Drugie polecenie używa polecenia cmdlet **Set-DscLocalConfigurationManager** w celu zastosowania metakonfiguracji do określonych komputerów w celu dotrzymania ich jako węzłów DSC.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="b8fd3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8fd3-115">PARAMETERS</span></span>

### <span data-ttu-id="b8fd3-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b8fd3-116">-AutomationAccountName</span></span>
<span data-ttu-id="b8fd3-117">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="b8fd3-118">Możesz dodać komputery, dla których parametr *ComputerName określa* konto, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8fd3-119">— Nazwa_komputera</span><span class="sxs-lookup"><span data-stu-id="b8fd3-119">-ComputerName</span></span>
<span data-ttu-id="b8fd3-120">Określa tablicę nazw komputerów, dla których to polecenie cmdlet generuje pliki mof.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="b8fd3-121">Jeśli nie określisz tego parametru, polecenie cmdlet wygeneruje plik mof dla bieżącego komputera (localhost).</span><span class="sxs-lookup"><span data-stu-id="b8fd3-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8fd3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8fd3-122">-DefaultProfile</span></span>
<span data-ttu-id="b8fd3-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b8fd3-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8fd3-124">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b8fd3-124">-Force</span></span>
<span data-ttu-id="b8fd3-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie i zamienianie istniejących plików mof o takich samych nazwach.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-125">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

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

### <span data-ttu-id="b8fd3-126">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="b8fd3-126">-OutputFolder</span></span>
<span data-ttu-id="b8fd3-127">Określa nazwę folderu, w którym to polecenie cmdlet przechowuje pliki mof.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-127">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

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

### <span data-ttu-id="b8fd3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8fd3-128">-ResourceGroupName</span></span>
<span data-ttu-id="b8fd3-129">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b8fd3-130">To polecenie cmdlet tworzy pliki mof na komputerach w grupie zasobów, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-130">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8fd3-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8fd3-131">-Confirm</span></span>
<span data-ttu-id="b8fd3-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8fd3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8fd3-133">-WhatIf</span></span>
<span data-ttu-id="b8fd3-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8fd3-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8fd3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8fd3-136">CommonParameters</span></span>
<span data-ttu-id="b8fd3-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8fd3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8fd3-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8fd3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8fd3-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8fd3-139">INPUTS</span></span>

### <span data-ttu-id="b8fd3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b8fd3-140">System.String</span></span>

### <span data-ttu-id="b8fd3-141">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b8fd3-141">System.String[]</span></span>

## <span data-ttu-id="b8fd3-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8fd3-142">OUTPUTS</span></span>

### <span data-ttu-id="b8fd3-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="b8fd3-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="b8fd3-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b8fd3-144">NOTES</span></span>

## <span data-ttu-id="b8fd3-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8fd3-145">RELATED LINKS</span></span>
