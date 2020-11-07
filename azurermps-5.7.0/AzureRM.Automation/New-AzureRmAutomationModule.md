---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: 91adec21cd620b0ac126a91191dba7ccdf0b3767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716646"
---
# <span data-ttu-id="f8908-101">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f8908-101">New-AzureRmAutomationModule</span></span>

## <span data-ttu-id="f8908-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8908-102">SYNOPSIS</span></span>
<span data-ttu-id="f8908-103">Importuje moduł do automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f8908-103">Imports a module into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8908-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8908-104">SYNTAX</span></span>

```
New-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8908-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f8908-105">DESCRIPTION</span></span>
<span data-ttu-id="f8908-106">Polecenie cmdlet **New-AzureRmAutomationModule** importuje moduł do usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f8908-106">The **New-AzureRmAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="f8908-107">To polecenie akceptuje plik skompresowany z rozszerzeniem nazwy pliku zip.</span><span class="sxs-lookup"><span data-stu-id="f8908-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="f8908-108">Plik zawiera folder zawierający plik z jednym z następujących typów:</span><span class="sxs-lookup"><span data-stu-id="f8908-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="f8908-109">Moduł wps_2, który ma rozszerzenie nazwy pliku PSM1 lub dll</span><span class="sxs-lookup"><span data-stu-id="f8908-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="f8908-110">Manifest modułu wps_2, który ma rozszerzenie nazwy pliku psd1</span><span class="sxs-lookup"><span data-stu-id="f8908-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="f8908-111">Nazwa pliku zip, nazwa folderu i nazwa pliku w tym folderze muszą być takie same.</span><span class="sxs-lookup"><span data-stu-id="f8908-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="f8908-112">Określ plik zip jako adres URL, do którego usługa automatyzacji może uzyskać dostęp.</span><span class="sxs-lookup"><span data-stu-id="f8908-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="f8908-113">W przypadku zaimportowania modułu wps_2 do automatyzacji za pomocą tego polecenia cmdlet lub polecenia cmdlet Set-AzureRmAutomationModule operacja jest asynchroniczna.</span><span class="sxs-lookup"><span data-stu-id="f8908-113">If you import a wps_2 module into Automation by using this cmdlet or the Set-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="f8908-114">Polecenie kończy się, czy importowanie powiedzie się, czy nie.</span><span class="sxs-lookup"><span data-stu-id="f8908-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="f8908-115">Aby sprawdzić, czy to powiodło, uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="f8908-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="f8908-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span><span class="sxs-lookup"><span data-stu-id="f8908-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="f8908-117">Sprawdź, czy właściwość **ProvisioningState** ma wartość pomyślną.</span><span class="sxs-lookup"><span data-stu-id="f8908-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="f8908-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8908-118">EXAMPLES</span></span>

### <span data-ttu-id="f8908-119">Przykład 1: Importowanie modułu</span><span class="sxs-lookup"><span data-stu-id="f8908-119">Example 1: Import a module</span></span>
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f8908-120">To polecenie importuje moduł o nazwie ContosoModule do konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f8908-120">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="f8908-121">Moduł jest przechowywany w obiekcie blob platformy Azure na koncie magazynu o nazwie contosostorage i kontenerze o nazwie moduły.</span><span class="sxs-lookup"><span data-stu-id="f8908-121">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="f8908-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8908-122">PARAMETERS</span></span>

### <span data-ttu-id="f8908-123">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f8908-123">-AutomationAccountName</span></span>
<span data-ttu-id="f8908-124">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet importuje moduł.</span><span class="sxs-lookup"><span data-stu-id="f8908-124">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8908-125">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="f8908-125">-ContentLinkUri</span></span>
<span data-ttu-id="f8908-126">Adres URL do pakietu zip modułu</span><span class="sxs-lookup"><span data-stu-id="f8908-126">The url to a module zip package</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8908-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8908-127">-DefaultProfile</span></span>
<span data-ttu-id="f8908-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f8908-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8908-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8908-129">-Name</span></span>
<span data-ttu-id="f8908-130">Określa nazwę modułu zaimportowanego za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8908-130">Specifies the name of the module that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8908-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8908-131">-ResourceGroupName</span></span>
<span data-ttu-id="f8908-132">Określa nazwę grupy zasobów, dla której to polecenie cmdlet importuje moduł.</span><span class="sxs-lookup"><span data-stu-id="f8908-132">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8908-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8908-133">CommonParameters</span></span>
<span data-ttu-id="f8908-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8908-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8908-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8908-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8908-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8908-136">INPUTS</span></span>

### <span data-ttu-id="f8908-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f8908-137">None</span></span>
<span data-ttu-id="f8908-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f8908-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8908-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8908-139">OUTPUTS</span></span>

### <span data-ttu-id="f8908-140">Microsoft. Azure. Commands. Automation. model. module</span><span class="sxs-lookup"><span data-stu-id="f8908-140">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="f8908-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8908-141">NOTES</span></span>

## <span data-ttu-id="f8908-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8908-142">RELATED LINKS</span></span>

[<span data-ttu-id="f8908-143">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f8908-143">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="f8908-144">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f8908-144">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="f8908-145">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f8908-145">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


