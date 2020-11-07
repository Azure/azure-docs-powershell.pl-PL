---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: d9c036c7047ee0d568f5e1451bce46dfe2903e29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706703"
---
# <span data-ttu-id="e6397-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e6397-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="e6397-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6397-102">SYNOPSIS</span></span>
<span data-ttu-id="e6397-103">Umożliwia zaktualizowanie modułu w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="e6397-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="e6397-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6397-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6397-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e6397-105">DESCRIPTION</span></span>
<span data-ttu-id="e6397-106">Polecenie cmdlet **Set-AzAutomationModule** aktualizuje moduł w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e6397-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="e6397-107">To polecenie akceptuje plik skompresowany z rozszerzeniem nazwy pliku zip.</span><span class="sxs-lookup"><span data-stu-id="e6397-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="e6397-108">Plik zawiera folder zawierający plik z jednym z następujących typów:</span><span class="sxs-lookup"><span data-stu-id="e6397-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="e6397-109">Moduł wps_2, który ma rozszerzenie nazwy pliku PSM1 lub dll</span><span class="sxs-lookup"><span data-stu-id="e6397-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="e6397-110">Manifest modułu wps_2, który ma rozszerzenie nazwy pliku psd1 nazwa pliku zip, nazwa folderu i nazwa pliku w folderze, muszą być takie same.</span><span class="sxs-lookup"><span data-stu-id="e6397-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="e6397-111">Określ plik zip jako adres URL, do którego usługa automatyzacji może uzyskać dostęp.</span><span class="sxs-lookup"><span data-stu-id="e6397-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="e6397-112">W przypadku zaimportowania modułu wps_2 do automatyzacji za pomocą tego polecenia cmdlet lub polecenia cmdlet New-AzAutomationModule operacja jest asynchroniczna.</span><span class="sxs-lookup"><span data-stu-id="e6397-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="e6397-113">Polecenie kończy się, czy importowanie powiedzie się, czy nie.</span><span class="sxs-lookup"><span data-stu-id="e6397-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="e6397-114">Aby sprawdzić, czy to powiodło, uruchom następujące polecenie: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName Sprawdź, czy właściwość **ProvisioningState** została pomyślnie zakończona.</span><span class="sxs-lookup"><span data-stu-id="e6397-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="e6397-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6397-115">EXAMPLES</span></span>

### <span data-ttu-id="e6397-116">Przykład 1: aktualizowanie modułu</span><span class="sxs-lookup"><span data-stu-id="e6397-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e6397-117">To polecenie importuje zaktualizowaną wersję istniejącego modułu o nazwie ContosoModule do konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e6397-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="e6397-118">Moduł jest przechowywany w obiekcie blob platformy Azure na koncie magazynu o nazwie contosostorage i kontenerze o nazwie moduły.</span><span class="sxs-lookup"><span data-stu-id="e6397-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="e6397-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6397-119">PARAMETERS</span></span>

### <span data-ttu-id="e6397-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e6397-120">-AutomationAccountName</span></span>
<span data-ttu-id="e6397-121">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet aktualizuje moduł.</span><span class="sxs-lookup"><span data-stu-id="e6397-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="e6397-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="e6397-122">-ContentLinkUri</span></span>
<span data-ttu-id="e6397-123">Określa adres URL pliku zip zawierającego nową wersję modułu, którego używa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6397-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6397-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="e6397-124">-ContentLinkVersion</span></span>
<span data-ttu-id="e6397-125">Określa wersję modułu, z którym to polecenie cmdlet aktualizuje automatyzację.</span><span class="sxs-lookup"><span data-stu-id="e6397-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="e6397-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6397-126">-DefaultProfile</span></span>
<span data-ttu-id="e6397-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e6397-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6397-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e6397-128">-Name</span></span>
<span data-ttu-id="e6397-129">Określa nazwę modułu zaimportowanego za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6397-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="e6397-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6397-130">-ResourceGroupName</span></span>
<span data-ttu-id="e6397-131">Określa nazwę grupy zasobów, dla której ten aplet polecenia zaktualizuje moduł.</span><span class="sxs-lookup"><span data-stu-id="e6397-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="e6397-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6397-132">CommonParameters</span></span>
<span data-ttu-id="e6397-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6397-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6397-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6397-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6397-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6397-135">INPUTS</span></span>

### <span data-ttu-id="e6397-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e6397-136">System.String</span></span>

### <span data-ttu-id="e6397-137">System. URI</span><span class="sxs-lookup"><span data-stu-id="e6397-137">System.Uri</span></span>

## <span data-ttu-id="e6397-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6397-138">OUTPUTS</span></span>

### <span data-ttu-id="e6397-139">Microsoft. Azure. Commands. Automation. model. module</span><span class="sxs-lookup"><span data-stu-id="e6397-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="e6397-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6397-140">NOTES</span></span>

## <span data-ttu-id="e6397-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6397-141">RELATED LINKS</span></span>

[<span data-ttu-id="e6397-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e6397-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="e6397-143">Nowe — AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e6397-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="e6397-144">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e6397-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)


