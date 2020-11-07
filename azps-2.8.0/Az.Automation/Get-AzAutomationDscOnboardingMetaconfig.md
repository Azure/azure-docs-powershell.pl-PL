---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 0302803568bac71baed28615552848f113da32df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706814"
---
# <span data-ttu-id="5a250-101">Get-AzAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="5a250-101">Get-AzAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="5a250-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a250-102">SYNOPSIS</span></span>
<span data-ttu-id="5a250-103">Tworzy plik meta-Configuration. mof.</span><span class="sxs-lookup"><span data-stu-id="5a250-103">Creates meta-configuration .mof files.</span></span>

## <span data-ttu-id="5a250-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a250-104">SYNTAX</span></span>

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a250-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5a250-105">DESCRIPTION</span></span>
<span data-ttu-id="5a250-106">Polecenie cmdlet **Get-AzAutomationDscOnboardingMetaconfig** powoduje utworzenie plików MOF (APS) o konfiguracji pożądanego stanu (DSC).</span><span class="sxs-lookup"><span data-stu-id="5a250-106">The **Get-AzAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="5a250-107">To polecenie cmdlet tworzy plik MOF dla każdej określonej nazwy komputera.</span><span class="sxs-lookup"><span data-stu-id="5a250-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="5a250-108">Polecenie cmdlet tworzy folder dla plików MOF.</span><span class="sxs-lookup"><span data-stu-id="5a250-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="5a250-109">Możesz uruchomić polecenie cmdlet Set-DscLocalConfigurationManager dla tego folderu, aby dołączać te komputery do konta usługi Azure Automation jako węzłów DSC.</span><span class="sxs-lookup"><span data-stu-id="5a250-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="5a250-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a250-110">EXAMPLES</span></span>

### <span data-ttu-id="5a250-111">Przykład 1: serwer dołączający do automatyzacji DSC</span><span class="sxs-lookup"><span data-stu-id="5a250-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="5a250-112">Pierwsze polecenie powoduje utworzenie plików meta konfiguracji DSC dla dwóch serwerów dla konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5a250-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="5a250-113">Polecenie zapisuje te pliki na komputerze stacjonarnym.</span><span class="sxs-lookup"><span data-stu-id="5a250-113">The command saves these files on a desktop.</span></span>
<span data-ttu-id="5a250-114">Drugie polecenie używa polecenia cmdlet **Set-DscLocalConfigurationManager** w celu zastosowania konfiguracji meta do określonych komputerów jako węzłów DSC.</span><span class="sxs-lookup"><span data-stu-id="5a250-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="5a250-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a250-115">PARAMETERS</span></span>

### <span data-ttu-id="5a250-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5a250-116">-AutomationAccountName</span></span>
<span data-ttu-id="5a250-117">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="5a250-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="5a250-118">Możesz dołączać komputery, które parametr *ComputerName* określa konto, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5a250-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="5a250-119">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="5a250-119">-ComputerName</span></span>
<span data-ttu-id="5a250-120">Określa tablicę nazw komputerów, dla których to polecenie cmdlet generuje pliki MOF.</span><span class="sxs-lookup"><span data-stu-id="5a250-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="5a250-121">Jeśli nie podano tego parametru, polecenie cmdlet generuje plik MOF dla bieżącego komputera (localhost).</span><span class="sxs-lookup"><span data-stu-id="5a250-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

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

### <span data-ttu-id="5a250-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a250-122">-DefaultProfile</span></span>
<span data-ttu-id="5a250-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5a250-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a250-124">-Force</span><span class="sxs-lookup"><span data-stu-id="5a250-124">-Force</span></span>
<span data-ttu-id="5a250-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie i zastąpienie istniejących plików MOF o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="5a250-125">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

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

### <span data-ttu-id="5a250-126">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="5a250-126">-OutputFolder</span></span>
<span data-ttu-id="5a250-127">Określa nazwę folderu, w którym to polecenie cmdlet przechowuje pliki MOF.</span><span class="sxs-lookup"><span data-stu-id="5a250-127">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

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

### <span data-ttu-id="5a250-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a250-128">-ResourceGroupName</span></span>
<span data-ttu-id="5a250-129">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5a250-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="5a250-130">To polecenie cmdlet tworzy pliki MOF na komputerach stacjonarnych w grupie zasobów, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="5a250-130">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5a250-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a250-131">-Confirm</span></span>
<span data-ttu-id="5a250-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a250-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a250-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a250-133">-WhatIf</span></span>
<span data-ttu-id="5a250-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a250-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a250-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5a250-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a250-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a250-136">CommonParameters</span></span>
<span data-ttu-id="5a250-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a250-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a250-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a250-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a250-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a250-139">INPUTS</span></span>

### <span data-ttu-id="5a250-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5a250-140">System.String</span></span>

### <span data-ttu-id="5a250-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="5a250-141">System.String[]</span></span>

## <span data-ttu-id="5a250-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a250-142">OUTPUTS</span></span>

### <span data-ttu-id="5a250-143">Microsoft. Azure. Commands. Automation. model. DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="5a250-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="5a250-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a250-144">NOTES</span></span>

## <span data-ttu-id="5a250-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a250-145">RELATED LINKS</span></span>