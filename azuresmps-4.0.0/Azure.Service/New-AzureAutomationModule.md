---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1F875179-E3CA-4BBB-822A-600777B2D980
online version: ''
schema: 2.0.0
ms.openlocfilehash: c93a09647e22f9d7f1c69cfd6aafe58799217686
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055189"
---
# <span data-ttu-id="9ddd9-101">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9ddd9-101">New-AzureAutomationModule</span></span>

## <span data-ttu-id="9ddd9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ddd9-102">SYNOPSIS</span></span>

<span data-ttu-id="9ddd9-103">Importuje moduł do automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="9ddd9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ddd9-104">SYNTAX</span></span>

```
New-AzureAutomationModule -Name <String> -ContentLink <Uri> [-Tags <IDictionary>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9ddd9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9ddd9-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="9ddd9-106">Polecenie cmdlet **New-AzureAutomationModule** importuje moduł do usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-106">The **New-AzureAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="9ddd9-107">Moduł to skompresowany plik z rozszerzeniem zip, który zawiera folder zawierający jedno z następujących typów plików:</span><span class="sxs-lookup"><span data-stu-id="9ddd9-107">A module is a compressed file, with a .zip extension, that contains a folder which includes one of the following file types:</span></span>

- <span data-ttu-id="9ddd9-108">Moduł programu Windows PowerShell (plik PSM1).</span><span class="sxs-lookup"><span data-stu-id="9ddd9-108">A Windows PowerShell module (psm1 file).</span></span> 

- <span data-ttu-id="9ddd9-109">Manifest modułu programu Windows PowerShell (plik psd1).</span><span class="sxs-lookup"><span data-stu-id="9ddd9-109">A Windows PowerShell module manifest (psd1 file).</span></span> 

- <span data-ttu-id="9ddd9-110">Zestaw (plik dll).</span><span class="sxs-lookup"><span data-stu-id="9ddd9-110">An assembly (dll file).</span></span>

<span data-ttu-id="9ddd9-111">Nazwy plików zip, folder w pliku zip i plik w folderze (. PSM1, PSD. 1 lub dll) muszą być zgodne.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-111">The names of the zip file, the folder in the zip file, and file in the folder (.psm1, psd.1, or .dll) must match.</span></span>

## <span data-ttu-id="9ddd9-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ddd9-112">EXAMPLES</span></span>

### <span data-ttu-id="9ddd9-113">Przykład 1: Importowanie modułu</span><span class="sxs-lookup"><span data-stu-id="9ddd9-113">Example 1: Import a module</span></span>
```
PS C:\> New-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip"
```

<span data-ttu-id="9ddd9-114">To polecenie importuje moduł o nazwie ContosoModule do konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-114">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="9ddd9-115">Moduł jest przechowywany w obiekcie blob platformy Azure na koncie magazynu o nazwie contosostorage i kontenerze o nazwie moduły.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-115">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="9ddd9-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ddd9-116">PARAMETERS</span></span>

### <span data-ttu-id="9ddd9-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9ddd9-117">-AutomationAccountName</span></span>
<span data-ttu-id="9ddd9-118">Określa nazwę konta automatyzacji, w którym będzie przechowywany moduł.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-118">Specifies the name of the Automation account the module will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ddd9-119">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="9ddd9-119">-ContentLink</span></span>
<span data-ttu-id="9ddd9-120">Publiczny adres URL, taki jak witryna sieci Web lub magazyn obiektów blob platformy Azure, określający ścieżkę do pliku modułu.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-120">Public URL such as a website or Azure blob storage specifying the path to the module file.</span></span>
<span data-ttu-id="9ddd9-121">To miejsce musi być dostępne publicznie.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-121">This location must be publically accessible.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ddd9-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9ddd9-122">-Name</span></span>
<span data-ttu-id="9ddd9-123">Określa nazwę modułu.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-123">Specifies a name for the module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ddd9-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="9ddd9-124">-Profile</span></span>
<span data-ttu-id="9ddd9-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9ddd9-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddd9-127">-Tagi</span><span class="sxs-lookup"><span data-stu-id="9ddd9-127">-Tags</span></span>
<span data-ttu-id="9ddd9-128">Określa co najmniej jeden znacznik powiązany z modułem.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-128">Specifies one or more tags related to the module.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ddd9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ddd9-129">CommonParameters</span></span>
<span data-ttu-id="9ddd9-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ddd9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ddd9-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ddd9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ddd9-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ddd9-132">INPUTS</span></span>

## <span data-ttu-id="9ddd9-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ddd9-133">OUTPUTS</span></span>

### <span data-ttu-id="9ddd9-134">Microsoft. Azure. Commands. Automation. model. module</span><span class="sxs-lookup"><span data-stu-id="9ddd9-134">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="9ddd9-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ddd9-135">NOTES</span></span>

## <span data-ttu-id="9ddd9-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ddd9-136">RELATED LINKS</span></span>

[<span data-ttu-id="9ddd9-137">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9ddd9-137">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="9ddd9-138">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9ddd9-138">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="9ddd9-139">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9ddd9-139">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


