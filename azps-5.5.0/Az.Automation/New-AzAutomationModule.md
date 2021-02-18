---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: c176c9b8726c4f0edfebcebdc77197f1d555807d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201066"
---
# <span data-ttu-id="187fc-101">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="187fc-101">New-AzAutomationModule</span></span>

## <span data-ttu-id="187fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="187fc-102">SYNOPSIS</span></span>
<span data-ttu-id="187fc-103">Importuje moduł do automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="187fc-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="187fc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="187fc-104">SYNTAX</span></span>

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="187fc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="187fc-105">DESCRIPTION</span></span>
<span data-ttu-id="187fc-106">Polecenie **cmdlet New-AzAutomationModule** importuje moduł do usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="187fc-106">The **New-AzAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="187fc-107">To polecenie akceptuje plik skompresowany z rozszerzeniem nazwy pliku zip.</span><span class="sxs-lookup"><span data-stu-id="187fc-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="187fc-108">Plik zawiera folder zawierający plik, który jest jednym z następujących typów:</span><span class="sxs-lookup"><span data-stu-id="187fc-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="187fc-109">Moduł Windows PowerShell z rozszerzeniem nazwy pliku psm1 lub dll</span><span class="sxs-lookup"><span data-stu-id="187fc-109">Windows PowerShell module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="187fc-110">Manifest modułu programu Windows PowerShell z rozszerzeniem nazwy pliku psd1 Nazwa pliku zip, nazwa folderu i nazwa pliku w folderze muszą być takie same.</span><span class="sxs-lookup"><span data-stu-id="187fc-110">Windows PowerShell module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="187fc-111">Określ plik zip jako adres URL, do który może uzyskać dostęp usługa automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="187fc-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="187fc-112">Jeśli zaimportujesz moduł programu Windows PowerShell do automatyzacji za pomocą tego polecenia cmdlet lub Set-AzAutomationModule cmdlet, operacja będzie asynchroniczna.</span><span class="sxs-lookup"><span data-stu-id="187fc-112">If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="187fc-113">Polecenie zakończy się powodzeniem lub niepowodzeniem importowania.</span><span class="sxs-lookup"><span data-stu-id="187fc-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="187fc-114">Aby sprawdzić, czy się powiodło, uruchom następujące polecenie: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName Check the **ProvisioningState property** for a value of Succeeded (Pomyślnie).</span><span class="sxs-lookup"><span data-stu-id="187fc-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="187fc-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="187fc-115">EXAMPLES</span></span>

### <span data-ttu-id="187fc-116">Przykład 1. Importowanie modułu</span><span class="sxs-lookup"><span data-stu-id="187fc-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="187fc-117">To polecenie importuje moduł o nazwie ContosoModule do konta automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="187fc-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="187fc-118">Moduł jest przechowywany w obiekcie blob platformy Azure na koncie magazynu o nazwie contosostorage i kontenerze o nazwach modułów.</span><span class="sxs-lookup"><span data-stu-id="187fc-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="187fc-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="187fc-119">PARAMETERS</span></span>

### <span data-ttu-id="187fc-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="187fc-120">-AutomationAccountName</span></span>
<span data-ttu-id="187fc-121">Określa nazwę konta automatyzacji, do którego to polecenie cmdlet importuje moduł.</span><span class="sxs-lookup"><span data-stu-id="187fc-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="187fc-122">- ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="187fc-122">-ContentLinkUri</span></span>
<span data-ttu-id="187fc-123">Adres URL pakietu zip modułu</span><span class="sxs-lookup"><span data-stu-id="187fc-123">The url to a module zip package</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187fc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="187fc-124">-DefaultProfile</span></span>
<span data-ttu-id="187fc-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="187fc-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="187fc-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="187fc-126">-Name</span></span>
<span data-ttu-id="187fc-127">Określa nazwę modułu importowanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="187fc-127">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="187fc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="187fc-128">-ResourceGroupName</span></span>
<span data-ttu-id="187fc-129">Określa nazwę grupy zasobów, dla której to polecenie cmdlet importuje moduł.</span><span class="sxs-lookup"><span data-stu-id="187fc-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="187fc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="187fc-130">CommonParameters</span></span>
<span data-ttu-id="187fc-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="187fc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="187fc-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="187fc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="187fc-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="187fc-133">INPUTS</span></span>

### <span data-ttu-id="187fc-134">System.String</span><span class="sxs-lookup"><span data-stu-id="187fc-134">System.String</span></span>

### <span data-ttu-id="187fc-135">System.Uri</span><span class="sxs-lookup"><span data-stu-id="187fc-135">System.Uri</span></span>

## <span data-ttu-id="187fc-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="187fc-136">OUTPUTS</span></span>

### <span data-ttu-id="187fc-137">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="187fc-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="187fc-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="187fc-138">NOTES</span></span>

## <span data-ttu-id="187fc-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="187fc-139">RELATED LINKS</span></span>

[<span data-ttu-id="187fc-140">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="187fc-140">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="187fc-141">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="187fc-141">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="187fc-142">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="187fc-142">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


