---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A920D84-0005-45A2-8229-FD9436A2CA6D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 927520466299776326229976b355444f9db6c23e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055015"
---
# <span data-ttu-id="9d482-101">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="9d482-101">Set-AzureService</span></span>

## <span data-ttu-id="9d482-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d482-102">SYNOPSIS</span></span>
<span data-ttu-id="9d482-103">Ustawia lub aktualizuje etykietę i opis określonej usługi Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9d482-103">Sets or updates the label and description of the specified Microsoft Azure service.</span></span>

## <span data-ttu-id="9d482-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d482-104">SYNTAX</span></span>

```
Set-AzureService [-ServiceName] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9d482-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9d482-105">DESCRIPTION</span></span>
<span data-ttu-id="9d482-106">Polecenie cmdlet **Set-AzureService** umożliwia przypisanie etykiety i opisu do usługi w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9d482-106">The **Set-AzureService** cmdlet assigns a label and description to a service in the current subscription.</span></span>

## <span data-ttu-id="9d482-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d482-107">EXAMPLES</span></span>

### <span data-ttu-id="9d482-108">Przykład 1: aktualizowanie etykiety i opisu usługi</span><span class="sxs-lookup"><span data-stu-id="9d482-108">Example 1: Update the label and description for a service</span></span>
```
PS C:\> C:\PS>Set-AzureService -ServiceName "MySvc1" -Label "MyTestSvc1" -Description "My service for testing out new configurations"
```

<span data-ttu-id="9d482-109">To polecenie ustawia etykietę na "MyTestSvc1" i opis "My Service do testowania nowych konfiguracji" dla usługi MyTestSvc1.</span><span class="sxs-lookup"><span data-stu-id="9d482-109">This command sets the label to "MyTestSvc1" and the description to "My service for testing out new configurations" for the MyTestSvc1 service.</span></span>

## <span data-ttu-id="9d482-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d482-110">PARAMETERS</span></span>

### <span data-ttu-id="9d482-111">— Opis</span><span class="sxs-lookup"><span data-stu-id="9d482-111">-Description</span></span>
<span data-ttu-id="9d482-112">Określa opis usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9d482-112">Specifies a description for the Azure service.</span></span>
<span data-ttu-id="9d482-113">Długość opisu może wynosić do 1024 znaków.</span><span class="sxs-lookup"><span data-stu-id="9d482-113">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d482-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9d482-114">-InformationAction</span></span>
<span data-ttu-id="9d482-115">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="9d482-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9d482-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9d482-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9d482-117">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="9d482-117">Continue</span></span>
- <span data-ttu-id="9d482-118">Ignorować</span><span class="sxs-lookup"><span data-stu-id="9d482-118">Ignore</span></span>
- <span data-ttu-id="9d482-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="9d482-119">Inquire</span></span>
- <span data-ttu-id="9d482-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9d482-120">SilentlyContinue</span></span>
- <span data-ttu-id="9d482-121">Przestaw</span><span class="sxs-lookup"><span data-stu-id="9d482-121">Stop</span></span>
- <span data-ttu-id="9d482-122">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="9d482-122">Suspend</span></span>

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

### <span data-ttu-id="9d482-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9d482-123">-InformationVariable</span></span>
<span data-ttu-id="9d482-124">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="9d482-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9d482-125">-Label</span><span class="sxs-lookup"><span data-stu-id="9d482-125">-Label</span></span>
<span data-ttu-id="9d482-126">Określa etykietę usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9d482-126">Specifies a label for the Azure service.</span></span>
<span data-ttu-id="9d482-127">Etykieta może mieć długość do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="9d482-127">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d482-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="9d482-128">-Profile</span></span>
<span data-ttu-id="9d482-129">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d482-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9d482-130">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9d482-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d482-131">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="9d482-131">-ReverseDnsFqdn</span></span>
<span data-ttu-id="9d482-132">Określa w pełni kwalifikowaną nazwę domeny dla zwrotnego DNS.</span><span class="sxs-lookup"><span data-stu-id="9d482-132">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d482-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9d482-133">-ServiceName</span></span>
<span data-ttu-id="9d482-134">Określa nazwę usługi platformy Azure do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="9d482-134">Specifies the name of the Azure service to update.</span></span>

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

### <span data-ttu-id="9d482-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d482-135">CommonParameters</span></span>
<span data-ttu-id="9d482-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d482-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d482-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d482-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d482-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d482-138">INPUTS</span></span>

## <span data-ttu-id="9d482-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d482-139">OUTPUTS</span></span>

### <span data-ttu-id="9d482-140">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="9d482-140">ManagementOperationContext</span></span>

## <span data-ttu-id="9d482-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d482-141">NOTES</span></span>

## <span data-ttu-id="9d482-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d482-142">RELATED LINKS</span></span>

[<span data-ttu-id="9d482-143">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="9d482-143">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="9d482-144">Nowe — AzureService</span><span class="sxs-lookup"><span data-stu-id="9d482-144">New-AzureService</span></span>](./New-AzureService.md)


