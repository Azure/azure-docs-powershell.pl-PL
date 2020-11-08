---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061870"
---
# <span data-ttu-id="9568e-101">New-WAPackQuickVM</span><span class="sxs-lookup"><span data-stu-id="9568e-101">New-WAPackQuickVM</span></span>

## <span data-ttu-id="9568e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9568e-102">SYNOPSIS</span></span>
<span data-ttu-id="9568e-103">Umożliwia utworzenie maszyny wirtualnej na podstawie szablonu.</span><span class="sxs-lookup"><span data-stu-id="9568e-103">Creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="9568e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9568e-104">SYNTAX</span></span>

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9568e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9568e-105">DESCRIPTION</span></span>
<span data-ttu-id="9568e-106">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="9568e-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="9568e-107">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9568e-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9568e-108">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9568e-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9568e-109">Polecenie cmdlet **New-WAPackQuickVM** umożliwia utworzenie maszyny wirtualnej na podstawie szablonu.</span><span class="sxs-lookup"><span data-stu-id="9568e-109">The **New-WAPackQuickVM** cmdlet creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="9568e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9568e-110">EXAMPLES</span></span>

### <span data-ttu-id="9568e-111">Przykład 1. Tworzenie maszyny wirtualnej na podstawie szablonu</span><span class="sxs-lookup"><span data-stu-id="9568e-111">Example 1: Create a virtual machine based on a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

<span data-ttu-id="9568e-112">Pierwsze polecenie tworzy obiekt **PSCredential** , a następnie zapisuje go w zmiennej $Credentials.</span><span class="sxs-lookup"><span data-stu-id="9568e-112">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="9568e-113">Polecenie cmdlet monituje o podanie konta i hasła.</span><span class="sxs-lookup"><span data-stu-id="9568e-113">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="9568e-114">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="9568e-114">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="9568e-115">Drugie polecenie pobiera szablon za pomocą polecenia cmdlet **Get-WAPackVMTemplate** .</span><span class="sxs-lookup"><span data-stu-id="9568e-115">The second command gets a template by using the **Get-WAPackVMTemplate** cmdlet.</span></span>
<span data-ttu-id="9568e-116">Polecenie określa identyfikator szablonu.</span><span class="sxs-lookup"><span data-stu-id="9568e-116">The command specifies the ID of a template.</span></span>
<span data-ttu-id="9568e-117">Polecenie zapisuje obiekt Template w zmiennej $TemplateID.</span><span class="sxs-lookup"><span data-stu-id="9568e-117">The command stores the template object in the $TemplateID variable.</span></span>

<span data-ttu-id="9568e-118">Polecenie ostatnie powoduje utworzenie maszyny wirtualnej o nazwie VirtualMachine023.</span><span class="sxs-lookup"><span data-stu-id="9568e-118">The final command creates a virtual machine named VirtualMachine023.</span></span>
<span data-ttu-id="9568e-119">Polecenie opiera się na maszynie wirtualnej na szablonie przechowywanym w $TemplateId.</span><span class="sxs-lookup"><span data-stu-id="9568e-119">The command bases the virtual machine on the template stored in $TemplateId.</span></span>

## <span data-ttu-id="9568e-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9568e-120">PARAMETERS</span></span>

### <span data-ttu-id="9568e-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9568e-121">-Name</span></span>
<span data-ttu-id="9568e-122">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9568e-122">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="9568e-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="9568e-123">-Profile</span></span>
<span data-ttu-id="9568e-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9568e-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9568e-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9568e-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9568e-126">— Szablon</span><span class="sxs-lookup"><span data-stu-id="9568e-126">-Template</span></span>
<span data-ttu-id="9568e-127">Określa szablon.</span><span class="sxs-lookup"><span data-stu-id="9568e-127">Specifies a template.</span></span>
<span data-ttu-id="9568e-128">Polecenie cmdlet umożliwia utworzenie maszyny wirtualnej na podstawie określonego szablonu.</span><span class="sxs-lookup"><span data-stu-id="9568e-128">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="9568e-129">Aby uzyskać obiekt szablonu, użyj polecenia cmdlet **Get-WAPackVMTemplate** .</span><span class="sxs-lookup"><span data-stu-id="9568e-129">To obtain a template object, use the **Get-WAPackVMTemplate** cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9568e-130">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="9568e-130">-VMCredential</span></span>
<span data-ttu-id="9568e-131">Określa poświadczenie dla lokalnego konta administratora.</span><span class="sxs-lookup"><span data-stu-id="9568e-131">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="9568e-132">Aby uzyskać obiekt **PSCredential** , użyj polecenia cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="9568e-132">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="9568e-133">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="9568e-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9568e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9568e-134">CommonParameters</span></span>
<span data-ttu-id="9568e-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9568e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9568e-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9568e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9568e-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9568e-137">INPUTS</span></span>

## <span data-ttu-id="9568e-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9568e-138">OUTPUTS</span></span>

## <span data-ttu-id="9568e-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9568e-139">NOTES</span></span>

## <span data-ttu-id="9568e-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9568e-140">RELATED LINKS</span></span>

[<span data-ttu-id="9568e-141">Nowe — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9568e-141">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="9568e-142">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="9568e-142">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)


