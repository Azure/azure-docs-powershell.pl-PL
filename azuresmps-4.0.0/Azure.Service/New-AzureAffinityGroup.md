---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 54C89A5F-BF94-468C-92E7-224808FDD0EC
online version: ''
schema: 2.0.0
ms.openlocfilehash: be84995e4826b79befc6282133d70f3ee4a79b4f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055193"
---
# <span data-ttu-id="2ed91-101">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="2ed91-101">New-AzureAffinityGroup</span></span>

## <span data-ttu-id="2ed91-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ed91-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed91-103">Tworzy grupę koligacji w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2ed91-103">Creates an affinity group in the current subscription.</span></span>

## <span data-ttu-id="2ed91-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ed91-104">SYNTAX</span></span>

```
New-AzureAffinityGroup [-Name] <String> [-Label <String>] [-Description <String>] -Location <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ed91-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2ed91-105">DESCRIPTION</span></span>
<span data-ttu-id="2ed91-106">Polecenie cmdlet **New-AzureAffinityGroup** umożliwia utworzenie grupy koligacji platformy Azure w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2ed91-106">The **New-AzureAffinityGroup** cmdlet creates an Azure affinity group in the current Azure subscription.</span></span>

<span data-ttu-id="2ed91-107">Grupa koligacji umożliwia umieszczanie usług i ich zasobów razem w systemie Azure Datacenter.</span><span class="sxs-lookup"><span data-stu-id="2ed91-107">An affinity group puts your services and their resources together in an Azure datacenter.</span></span>
<span data-ttu-id="2ed91-108">Grupa koligacji umożliwia zespołom współdziałanie wszystkich użytkowników w celu zapewnienia optymalnej wydajności.</span><span class="sxs-lookup"><span data-stu-id="2ed91-108">The affinity group groups members together for optimal performance.</span></span>
<span data-ttu-id="2ed91-109">Definiowanie grup koligacji na poziomie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="2ed91-109">Define affinity groups at the subscription level.</span></span>
<span data-ttu-id="2ed91-110">Grupy koligacji są dostępne dla wszystkich kolejnych usług w chmurze lub kont magazynu, które utworzysz.</span><span class="sxs-lookup"><span data-stu-id="2ed91-110">Your affinity groups are available to any subsequent cloud services or storage accounts that you create.</span></span>
<span data-ttu-id="2ed91-111">Usługi można dodawać do grupy koligacji tylko po jej utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="2ed91-111">You can add services to an affinity group only when you create it.</span></span>

## <span data-ttu-id="2ed91-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ed91-112">EXAMPLES</span></span>

### <span data-ttu-id="2ed91-113">Przykład 1. Tworzenie grupy koligacji</span><span class="sxs-lookup"><span data-stu-id="2ed91-113">Example 1: Create an affinity group</span></span>
```
PS C:\> New-AzureAffinityGroup -Name "South01" -Location "South Central US" -Label "South Region" -Description "Affinity group for production applications in southern region."
```

<span data-ttu-id="2ed91-114">To polecenie tworzy grupę koligacji o nazwie South01 w regionie Południowo-środkowe w Stanach Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="2ed91-114">This command creates an affinity group named South01 in the South Central US region.</span></span>
<span data-ttu-id="2ed91-115">Polecenie Określa etykietę i opis.</span><span class="sxs-lookup"><span data-stu-id="2ed91-115">The command specifies a label and a description.</span></span>

## <span data-ttu-id="2ed91-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ed91-116">PARAMETERS</span></span>

### <span data-ttu-id="2ed91-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="2ed91-117">-Description</span></span>
<span data-ttu-id="2ed91-118">Określa opis grupy koligacji.</span><span class="sxs-lookup"><span data-stu-id="2ed91-118">Specifies a description for the affinity group.</span></span>
<span data-ttu-id="2ed91-119">Długość opisu może wynosić do 1024 znaków.</span><span class="sxs-lookup"><span data-stu-id="2ed91-119">The description may be up to 1024 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed91-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2ed91-120">-InformationAction</span></span>
<span data-ttu-id="2ed91-121">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="2ed91-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2ed91-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2ed91-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2ed91-123">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="2ed91-123">Continue</span></span>
- <span data-ttu-id="2ed91-124">Ignorować</span><span class="sxs-lookup"><span data-stu-id="2ed91-124">Ignore</span></span>
- <span data-ttu-id="2ed91-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="2ed91-125">Inquire</span></span>
- <span data-ttu-id="2ed91-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2ed91-126">SilentlyContinue</span></span>
- <span data-ttu-id="2ed91-127">Przestaw</span><span class="sxs-lookup"><span data-stu-id="2ed91-127">Stop</span></span>
- <span data-ttu-id="2ed91-128">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="2ed91-128">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed91-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2ed91-129">-InformationVariable</span></span>
<span data-ttu-id="2ed91-130">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="2ed91-130">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed91-131">-Label</span><span class="sxs-lookup"><span data-stu-id="2ed91-131">-Label</span></span>
<span data-ttu-id="2ed91-132">Określa etykietę grupy koligacji.</span><span class="sxs-lookup"><span data-stu-id="2ed91-132">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="2ed91-133">Etykieta może mieć długość do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="2ed91-133">The label may be up to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed91-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2ed91-134">-Location</span></span>
<span data-ttu-id="2ed91-135">Określa lokalizację geograficzną systemu Azure Datacenter, w którym to polecenie cmdlet tworzy grupę koligacji.</span><span class="sxs-lookup"><span data-stu-id="2ed91-135">Specifies the geographical location of the Azure datacenter where this cmdlet creates the affinity group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed91-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2ed91-136">-Name</span></span>
<span data-ttu-id="2ed91-137">Określa nazwę grupy koligacji.</span><span class="sxs-lookup"><span data-stu-id="2ed91-137">Specifies a name for the affinity group.</span></span>
<span data-ttu-id="2ed91-138">Nazwa musi być unikatowa dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2ed91-138">The name must be unique to the subscription.</span></span>

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

### <span data-ttu-id="2ed91-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="2ed91-139">-Profile</span></span>
<span data-ttu-id="2ed91-140">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ed91-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2ed91-141">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2ed91-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2ed91-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed91-142">CommonParameters</span></span>
<span data-ttu-id="2ed91-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ed91-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed91-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ed91-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed91-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ed91-145">INPUTS</span></span>

## <span data-ttu-id="2ed91-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ed91-146">OUTPUTS</span></span>

## <span data-ttu-id="2ed91-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ed91-147">NOTES</span></span>

## <span data-ttu-id="2ed91-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ed91-148">RELATED LINKS</span></span>

[<span data-ttu-id="2ed91-149">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="2ed91-149">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="2ed91-150">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="2ed91-150">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="2ed91-151">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="2ed91-151">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


