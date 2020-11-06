---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
ms.openlocfilehash: a0c3693220ab614dcb84d69bc8c17a0ad632a2b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528310"
---
# <span data-ttu-id="fcbfd-101">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fcbfd-101">Set-AzureRmAutomationModule</span></span>

## <span data-ttu-id="fcbfd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fcbfd-102">SYNOPSIS</span></span>
<span data-ttu-id="fcbfd-103">Umożliwia zaktualizowanie modułu w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="fcbfd-103">Updates a module in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcbfd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fcbfd-104">SYNTAX</span></span>

```
Set-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fcbfd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fcbfd-105">DESCRIPTION</span></span>
<span data-ttu-id="fcbfd-106">Polecenie cmdlet **Set-AzureRmAutomationModule** aktualizuje moduł w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="fcbfd-106">The **Set-AzureRmAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="fcbfd-107">To polecenie akceptuje plik skompresowany z rozszerzeniem nazwy pliku zip.</span><span class="sxs-lookup"><span data-stu-id="fcbfd-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="fcbfd-108">Plik zawiera folder zawierający plik z jednym z następujących typów:</span><span class="sxs-lookup"><span data-stu-id="fcbfd-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="fcbfd-109">Moduł wps_2, który ma rozszerzenie nazwy pliku PSM1 lub dll</span><span class="sxs-lookup"><span data-stu-id="fcbfd-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="fcbfd-110">Manifest modułu wps_2, który ma rozszerzenie nazwy pliku psd1</span><span class="sxs-lookup"><span data-stu-id="fcbfd-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="fcbfd-111">Nazwa pliku zip, nazwa folderu i nazwa pliku w tym folderze muszą być takie same.</span><span class="sxs-lookup"><span data-stu-id="fcbfd-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="fcbfd-112">Określ plik zip jako adres URL, do którego usługa automatyzacji może uzyskać dostęp.</span><span class="sxs-lookup"><span data-stu-id="fcbfd-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="fcbfd-113">W przypadku zaimportowania modułu wps_2 do automatyzacji za pomocą tego polecenia cmdlet lub polecenia cmdlet New-AzureRmAutomationModule operacja jest asynchroniczna.</span><span class="sxs-lookup"><span data-stu-id="fcbfd-113">If you import a wps_2 module into Automation by using this cmdlet or the New-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="fcbfd-114">Polecenie kończy się, czy importowanie powiedzie się, czy nie.</span><span class="sxs-lookup"><span data-stu-id="fcbfd-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="fcbfd-115">Aby sprawdzić, czy to powiodło, uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="fcbfd-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="fcbfd-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span><span class="sxs-lookup"><span data-stu-id="fcbfd-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="fcbfd-117">Sprawdź, czy właściwość **ProvisioningState** ma wartość pomyślną.</span><span class="sxs-lookup"><span data-stu-id="fcbfd-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="fcbfd-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fcbfd-118">EXAMPLES</span></span>

### <span data-ttu-id="fcbfd-119">Przykład 1: aktualizowanie modułu</span><span class="sxs-lookup"><span data-stu-id="fcbfd-119">Example 1: Update a module</span></span>
```
PS C:\>Set-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fcbfd-120">To polecenie importuje zaktualizowaną wersję istniejącego modułu o nazwie ContosoModule do konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="fcbfd-120">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>

## <span data-ttu-id="fcbfd-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fcbfd-121">PARAMETERS</span></span>

### <span data-ttu-id="fcbfd-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fcbfd-122">-AutomationAccountName</span></span>
<span data-ttu-id="fcbfd-123">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet aktualizuje moduł.</span><span class="sxs-lookup"><span data-stu-id="fcbfd-123">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="fcbfd-124">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="fcbfd-124">-ContentLinkUri</span></span>
<span data-ttu-id="fcbfd-125">Określa adres URL pliku zip zawierającego nową wersję modułu, którego używa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcbfd-125">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="fcbfd-126">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="fcbfd-126">-ContentLinkVersion</span></span>
<span data-ttu-id="fcbfd-127">Określa wersję modułu, z którym to polecenie cmdlet aktualizuje automatyzację.</span><span class="sxs-lookup"><span data-stu-id="fcbfd-127">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="fcbfd-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fcbfd-128">-Name</span></span>
<span data-ttu-id="fcbfd-129">Określa nazwę modułu zaimportowanego za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcbfd-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="fcbfd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcbfd-130">-ResourceGroupName</span></span>
<span data-ttu-id="fcbfd-131">Określa nazwę grupy zasobów, dla której ten aplet polecenia zaktualizuje moduł.</span><span class="sxs-lookup"><span data-stu-id="fcbfd-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="fcbfd-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcbfd-132">-DefaultProfile</span></span>
<span data-ttu-id="fcbfd-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fcbfd-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcbfd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcbfd-134">CommonParameters</span></span>
<span data-ttu-id="fcbfd-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcbfd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcbfd-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcbfd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcbfd-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcbfd-137">INPUTS</span></span>

## <span data-ttu-id="fcbfd-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fcbfd-138">OUTPUTS</span></span>

### <span data-ttu-id="fcbfd-139">Microsoft. Azure. Commands. Automation. model. module</span><span class="sxs-lookup"><span data-stu-id="fcbfd-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="fcbfd-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fcbfd-140">NOTES</span></span>

## <span data-ttu-id="fcbfd-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcbfd-141">RELATED LINKS</span></span>

[<span data-ttu-id="fcbfd-142">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fcbfd-142">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="fcbfd-143">Nowe — AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fcbfd-143">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="fcbfd-144">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fcbfd-144">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)


