---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3422EFD0-88DC-4DF0-868C-5C63C9FA95EF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9aa78f34abf17c2aa5858697f492f76ee124d91
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054656"
---
# <span data-ttu-id="2888e-101">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2888e-101">Disable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="2888e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2888e-102">SYNOPSIS</span></span>
<span data-ttu-id="2888e-103">Wyłącza program Application Diagnostics dla witryny internetowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2888e-103">Disables application diagnostics for an Azure website.</span></span>

## <span data-ttu-id="2888e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2888e-104">SYNTAX</span></span>

```
Disable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] [-TableStorage] [-BlobStorage] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2888e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2888e-105">DESCRIPTION</span></span>
<span data-ttu-id="2888e-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2888e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2888e-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2888e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2888e-108">Wyłącza program Application Diagnostics dla witryny internetowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2888e-108">Disables application diagnostics for an Azure website.</span></span>
<span data-ttu-id="2888e-109">Wyłącza rejestrowanie skonfigurowane do przechowywania w systemie plików lub na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="2888e-109">Disables logging configured to be stored on a file system or on Azure.</span></span>

## <span data-ttu-id="2888e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2888e-110">EXAMPLES</span></span>

### <span data-ttu-id="2888e-111">Przykład 1. wyłączanie pliku dziennika aplikacji</span><span class="sxs-lookup"><span data-stu-id="2888e-111">Example 1:  Disable application logging file</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File
```

<span data-ttu-id="2888e-112">Poniższy przykład wyłącza rejestrowanie aplikacji w systemie plików.</span><span class="sxs-lookup"><span data-stu-id="2888e-112">The following example disables application logging on the file system.</span></span>

### <span data-ttu-id="2888e-113">Przykład 2: wyłączenie rejestrowania w usłudze Azure Storage</span><span class="sxs-lookup"><span data-stu-id="2888e-113">Example 2:  Disable logging using Azure storage</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage
```

<span data-ttu-id="2888e-114">Poniższy przykład wyłącza rejestrowanie aplikacji przy użyciu magazynu.</span><span class="sxs-lookup"><span data-stu-id="2888e-114">The following example disables application logging using storage.</span></span>

## <span data-ttu-id="2888e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2888e-115">PARAMETERS</span></span>

### <span data-ttu-id="2888e-116">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="2888e-116">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2888e-117">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="2888e-117">-File</span></span>
<span data-ttu-id="2888e-118">Określa, że chcesz używać systemu plików do przechowywania plików dziennika.</span><span class="sxs-lookup"><span data-stu-id="2888e-118">Specifies that you want to use the file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2888e-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2888e-119">-Name</span></span>
<span data-ttu-id="2888e-120">Określa nazwę witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="2888e-120">Specifies the name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2888e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2888e-121">-PassThru</span></span>
<span data-ttu-id="2888e-122">Flaga zwracająca wartość PRAWDA, jeśli powiodła się.</span><span class="sxs-lookup"><span data-stu-id="2888e-122">Flag to return true if succeeded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2888e-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="2888e-123">-Profile</span></span>
<span data-ttu-id="2888e-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2888e-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2888e-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2888e-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2888e-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="2888e-126">-Slot</span></span>
<span data-ttu-id="2888e-127">Określa nazwę gniazda.</span><span class="sxs-lookup"><span data-stu-id="2888e-127">Specifies the name of slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2888e-128">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="2888e-128">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2888e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2888e-129">CommonParameters</span></span>
<span data-ttu-id="2888e-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2888e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2888e-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2888e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2888e-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2888e-132">INPUTS</span></span>

## <span data-ttu-id="2888e-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2888e-133">OUTPUTS</span></span>

## <span data-ttu-id="2888e-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2888e-134">NOTES</span></span>

## <span data-ttu-id="2888e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2888e-135">RELATED LINKS</span></span>

[<span data-ttu-id="2888e-136">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2888e-136">Enable-AzureWebsiteApplicationDiagnostic</span></span>](./Enable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="2888e-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2888e-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="2888e-138">Nowe — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2888e-138">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="2888e-139">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2888e-139">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="2888e-140">Start — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2888e-140">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


