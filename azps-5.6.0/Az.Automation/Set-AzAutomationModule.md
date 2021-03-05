---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 475c4ab3105aa8ae01543c0f3674d5d119604a2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009825"
---
# <span data-ttu-id="11718-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="11718-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="11718-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11718-102">SYNOPSIS</span></span>
<span data-ttu-id="11718-103">Aktualizuje moduł w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="11718-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="11718-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11718-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11718-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="11718-105">DESCRIPTION</span></span>
<span data-ttu-id="11718-106">Polecenie **cmdlet Set-AzAutomationModule** aktualizuje moduł w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="11718-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="11718-107">To polecenie akceptuje plik skompresowany z rozszerzeniem nazwy pliku zip.</span><span class="sxs-lookup"><span data-stu-id="11718-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="11718-108">Plik zawiera folder zawierający plik, który jest jednym z następujących typów:</span><span class="sxs-lookup"><span data-stu-id="11718-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="11718-109">wps_2, który ma rozszerzenie nazwy pliku psm1 lub dll</span><span class="sxs-lookup"><span data-stu-id="11718-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="11718-110">wps_2 manifestu modułu, który ma rozszerzenie nazwy pliku psd1: nazwa pliku zip, nazwa folderu i nazwa pliku w folderze muszą być takie same.</span><span class="sxs-lookup"><span data-stu-id="11718-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="11718-111">Określ plik zip jako adres URL, do który może uzyskać dostęp usługa automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="11718-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="11718-112">W przypadku importowania modułu wps_2 do automatyzacji za pomocą tego polecenia cmdlet lub New-AzAutomationModule cmdlet operacja jest asynchroniczna.</span><span class="sxs-lookup"><span data-stu-id="11718-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="11718-113">Polecenie zakończy się powodzeniem lub niepowodzeniem importowania.</span><span class="sxs-lookup"><span data-stu-id="11718-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="11718-114">Aby sprawdzić, czy się powiodło, uruchom następujące polecenie: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName Check the **ProvisioningState property** for a value of Succeeded (Pomyślnie).</span><span class="sxs-lookup"><span data-stu-id="11718-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="11718-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11718-115">EXAMPLES</span></span>

### <span data-ttu-id="11718-116">Przykład 1. Aktualizowanie modułu</span><span class="sxs-lookup"><span data-stu-id="11718-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="11718-117">To polecenie importuje zaktualizowaną wersję istniejącego modułu o nazwie ContosoModule do konta automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="11718-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="11718-118">Moduł jest przechowywany w obiekcie blob platformy Azure na koncie magazynu o nazwie contosostorage i kontenerze o nazwanych modułach.</span><span class="sxs-lookup"><span data-stu-id="11718-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="11718-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11718-119">PARAMETERS</span></span>

### <span data-ttu-id="11718-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="11718-120">-AutomationAccountName</span></span>
<span data-ttu-id="11718-121">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet aktualizuje moduł.</span><span class="sxs-lookup"><span data-stu-id="11718-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="11718-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="11718-122">-ContentLinkUri</span></span>
<span data-ttu-id="11718-123">Określa adres URL pliku zip zawierającego nową wersję modułu importowanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11718-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="11718-124">- ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="11718-124">-ContentLinkVersion</span></span>
<span data-ttu-id="11718-125">Określa wersję modułu, dla którego to polecenie cmdlet aktualizuje automatyzację.</span><span class="sxs-lookup"><span data-stu-id="11718-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="11718-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11718-126">-DefaultProfile</span></span>
<span data-ttu-id="11718-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="11718-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11718-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="11718-128">-Name</span></span>
<span data-ttu-id="11718-129">Określa nazwę modułu importowanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11718-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="11718-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11718-130">-ResourceGroupName</span></span>
<span data-ttu-id="11718-131">Określa nazwę grupy zasobów, dla której to polecenie cmdlet aktualizuje moduł.</span><span class="sxs-lookup"><span data-stu-id="11718-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="11718-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11718-132">CommonParameters</span></span>
<span data-ttu-id="11718-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11718-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11718-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11718-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11718-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11718-135">INPUTS</span></span>

### <span data-ttu-id="11718-136">System.String</span><span class="sxs-lookup"><span data-stu-id="11718-136">System.String</span></span>

### <span data-ttu-id="11718-137">System.Uri</span><span class="sxs-lookup"><span data-stu-id="11718-137">System.Uri</span></span>

## <span data-ttu-id="11718-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11718-138">OUTPUTS</span></span>

### <span data-ttu-id="11718-139">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="11718-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="11718-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11718-140">NOTES</span></span>

## <span data-ttu-id="11718-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11718-141">RELATED LINKS</span></span>

[<span data-ttu-id="11718-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="11718-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="11718-143">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="11718-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="11718-144">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="11718-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)


