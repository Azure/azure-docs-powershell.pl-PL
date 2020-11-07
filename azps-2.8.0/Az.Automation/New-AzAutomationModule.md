---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: 7e9b2e9a87cc9a02c807a2eae3b64e7a13c87a1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706765"
---
# <span data-ttu-id="d04c6-101">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d04c6-101">New-AzAutomationModule</span></span>

## <span data-ttu-id="d04c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d04c6-102">SYNOPSIS</span></span>
<span data-ttu-id="d04c6-103">Importuje moduł do automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="d04c6-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="d04c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d04c6-104">SYNTAX</span></span>

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d04c6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d04c6-105">DESCRIPTION</span></span>
<span data-ttu-id="d04c6-106">Polecenie cmdlet **New-AzAutomationModule** importuje moduł do usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d04c6-106">The **New-AzAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="d04c6-107">To polecenie akceptuje plik skompresowany z rozszerzeniem nazwy pliku zip.</span><span class="sxs-lookup"><span data-stu-id="d04c6-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="d04c6-108">Plik zawiera folder zawierający plik z jednym z następujących typów:</span><span class="sxs-lookup"><span data-stu-id="d04c6-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="d04c6-109">Moduł programu Windows PowerShell z rozszerzeniem nazwy pliku PSM1 lub dll</span><span class="sxs-lookup"><span data-stu-id="d04c6-109">Windows PowerShell module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="d04c6-110">Manifest modułu programu Windows PowerShell z rozszerzeniem nazwy pliku psd1 nazwa pliku. zip, nazwa folderu i nazwa pliku w folderze muszą być takie same, jak w przypadku tej samej nazwy.</span><span class="sxs-lookup"><span data-stu-id="d04c6-110">Windows PowerShell module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="d04c6-111">Określ plik zip jako adres URL, do którego usługa automatyzacji może uzyskać dostęp.</span><span class="sxs-lookup"><span data-stu-id="d04c6-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="d04c6-112">W przypadku zaimportowania modułu programu Windows PowerShell do automatyzacji za pomocą tego polecenia cmdlet lub polecenia cmdlet Set-AzAutomationModule operacja jest asynchroniczna.</span><span class="sxs-lookup"><span data-stu-id="d04c6-112">If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="d04c6-113">Polecenie kończy się, czy importowanie powiedzie się, czy nie.</span><span class="sxs-lookup"><span data-stu-id="d04c6-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="d04c6-114">Aby sprawdzić, czy to powiodło, uruchom następujące polecenie: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName Sprawdź, czy właściwość **ProvisioningState** została pomyślnie zakończona.</span><span class="sxs-lookup"><span data-stu-id="d04c6-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="d04c6-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d04c6-115">EXAMPLES</span></span>

### <span data-ttu-id="d04c6-116">Przykład 1: Importowanie modułu</span><span class="sxs-lookup"><span data-stu-id="d04c6-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d04c6-117">To polecenie importuje moduł o nazwie ContosoModule do konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d04c6-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="d04c6-118">Moduł jest przechowywany w obiekcie blob platformy Azure na koncie magazynu o nazwie contosostorage i kontenerze o nazwie moduły.</span><span class="sxs-lookup"><span data-stu-id="d04c6-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="d04c6-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d04c6-119">PARAMETERS</span></span>

### <span data-ttu-id="d04c6-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d04c6-120">-AutomationAccountName</span></span>
<span data-ttu-id="d04c6-121">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet importuje moduł.</span><span class="sxs-lookup"><span data-stu-id="d04c6-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="d04c6-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="d04c6-122">-ContentLinkUri</span></span>
<span data-ttu-id="d04c6-123">Adres URL do pakietu zip modułu</span><span class="sxs-lookup"><span data-stu-id="d04c6-123">The url to a module zip package</span></span>

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

### <span data-ttu-id="d04c6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d04c6-124">-DefaultProfile</span></span>
<span data-ttu-id="d04c6-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d04c6-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d04c6-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d04c6-126">-Name</span></span>
<span data-ttu-id="d04c6-127">Określa nazwę modułu zaimportowanego za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d04c6-127">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="d04c6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d04c6-128">-ResourceGroupName</span></span>
<span data-ttu-id="d04c6-129">Określa nazwę grupy zasobów, dla której to polecenie cmdlet importuje moduł.</span><span class="sxs-lookup"><span data-stu-id="d04c6-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="d04c6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d04c6-130">CommonParameters</span></span>
<span data-ttu-id="d04c6-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d04c6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d04c6-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d04c6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d04c6-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d04c6-133">INPUTS</span></span>

### <span data-ttu-id="d04c6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d04c6-134">System.String</span></span>

### <span data-ttu-id="d04c6-135">System. URI</span><span class="sxs-lookup"><span data-stu-id="d04c6-135">System.Uri</span></span>

## <span data-ttu-id="d04c6-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d04c6-136">OUTPUTS</span></span>

### <span data-ttu-id="d04c6-137">Microsoft. Azure. Commands. Automation. model. module</span><span class="sxs-lookup"><span data-stu-id="d04c6-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="d04c6-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d04c6-138">NOTES</span></span>

## <span data-ttu-id="d04c6-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d04c6-139">RELATED LINKS</span></span>

[<span data-ttu-id="d04c6-140">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d04c6-140">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="d04c6-141">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d04c6-141">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="d04c6-142">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d04c6-142">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)

