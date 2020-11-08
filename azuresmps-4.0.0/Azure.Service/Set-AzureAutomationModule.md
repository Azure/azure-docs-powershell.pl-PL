---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 9CED6E53-B65C-4D55-8AC7-9E8A8B143544
online version: ''
schema: 2.0.0
ms.openlocfilehash: da8f0e3bdc9e1cf573e9189e49feda85ee8c1b90
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054796"
---
# <span data-ttu-id="42d8d-101">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="42d8d-101">Set-AzureAutomationModule</span></span>

## <span data-ttu-id="42d8d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42d8d-102">SYNOPSIS</span></span>

<span data-ttu-id="42d8d-103">Umożliwia zaktualizowanie modułu w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="42d8d-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="42d8d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42d8d-104">SYNTAX</span></span>

```
Set-AzureAutomationModule -Name <String> [-Tags <IDictionary>] [-ContentLinkUri <Uri>]
 [-ContentLinkVersion <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="42d8d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="42d8d-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="42d8d-106">Polecenie cmdlet **Set-AzureAutomationModule** powoduje zaimportowanie nowej wersji modułu lub zmianę konfiguracji modułu w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="42d8d-106">The **Set-AzureAutomationModule** cmdlet imports a new version of a module or changes the configuration of the module in Azure Automation.</span></span>

## <span data-ttu-id="42d8d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42d8d-107">EXAMPLES</span></span>

### <span data-ttu-id="42d8d-108">Przykład 1: aktualizowanie modułu</span><span class="sxs-lookup"><span data-stu-id="42d8d-108">Example 1: Update a module</span></span>
```
PS C:\> Set-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1"
```

<span data-ttu-id="42d8d-109">To polecenie importuje zaktualizowaną wersję istniejącego modułu o nazwie ContosoModule na konto usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="42d8d-109">This command imports an updated version of an existing module named ContosoModule into the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="42d8d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42d8d-110">PARAMETERS</span></span>

### <span data-ttu-id="42d8d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="42d8d-111">-AutomationAccountName</span></span>
<span data-ttu-id="42d8d-112">Określa nazwę konta automatyzacji z modułem.</span><span class="sxs-lookup"><span data-stu-id="42d8d-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="42d8d-113">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="42d8d-113">-ContentLinkUri</span></span>
<span data-ttu-id="42d8d-114">Określa ścieżkę do pliku modułu.</span><span class="sxs-lookup"><span data-stu-id="42d8d-114">Specifies the path to the module file.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d8d-115">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="42d8d-115">-ContentLinkVersion</span></span>
<span data-ttu-id="42d8d-116">Określa wersję modułu.</span><span class="sxs-lookup"><span data-stu-id="42d8d-116">Specifies the version of the module.</span></span>

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

### <span data-ttu-id="42d8d-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="42d8d-117">-Name</span></span>
<span data-ttu-id="42d8d-118">Określa nazwę modułu.</span><span class="sxs-lookup"><span data-stu-id="42d8d-118">Specifies the name of the module.</span></span>

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

### <span data-ttu-id="42d8d-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="42d8d-119">-Profile</span></span>
<span data-ttu-id="42d8d-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42d8d-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="42d8d-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="42d8d-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="42d8d-122">-Tagi</span><span class="sxs-lookup"><span data-stu-id="42d8d-122">-Tags</span></span>
<span data-ttu-id="42d8d-123">Określa Tagi modułu.</span><span class="sxs-lookup"><span data-stu-id="42d8d-123">Specifies tags for the module.</span></span>

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

### <span data-ttu-id="42d8d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d8d-124">CommonParameters</span></span>
<span data-ttu-id="42d8d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42d8d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d8d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d8d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d8d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42d8d-127">INPUTS</span></span>

### <span data-ttu-id="42d8d-128">Microsoft. Azure. Commands. Automation. model. module</span><span class="sxs-lookup"><span data-stu-id="42d8d-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="42d8d-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42d8d-129">OUTPUTS</span></span>

## <span data-ttu-id="42d8d-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42d8d-130">NOTES</span></span>

## <span data-ttu-id="42d8d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42d8d-131">RELATED LINKS</span></span>

[<span data-ttu-id="42d8d-132">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="42d8d-132">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="42d8d-133">Nowe — AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="42d8d-133">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="42d8d-134">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="42d8d-134">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)


