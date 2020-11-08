---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055341"
---
# <span data-ttu-id="3a331-101">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3a331-101">Enable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="3a331-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a331-102">SYNOPSIS</span></span>
<span data-ttu-id="3a331-103">Włącza profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="3a331-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="3a331-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a331-104">SYNTAX</span></span>

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3a331-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a331-105">DESCRIPTION</span></span>
<span data-ttu-id="3a331-106">Polecenie cmdlet **enable-AzureTrafficManagerProfile** umożliwia profilowi Microsoft Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="3a331-106">The **Enable-AzureTrafficManagerProfile** cmdlet enables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="3a331-107">Określ parametr *PassThru* , aby wyświetlić, czy operacja powiodła się.</span><span class="sxs-lookup"><span data-stu-id="3a331-107">Specify the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="3a331-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a331-108">EXAMPLES</span></span>

### <span data-ttu-id="3a331-109">Przykład 1: Włączanie profilu w usłudze Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="3a331-109">Example 1: Enable a Traffic Manager profile</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="3a331-110">To polecenie włącza profil usługi Traffic Manager o nazwie Moja profil.</span><span class="sxs-lookup"><span data-stu-id="3a331-110">This command enables the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="3a331-111">Przykład 2: Włączanie profilu usługi Traffic Manager i wyświetlanie wyników</span><span class="sxs-lookup"><span data-stu-id="3a331-111">Example 2: Enable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="3a331-112">To polecenie umożliwia włączenie profilu usługi Traffic Manager o nazwie Moja profil i wyświetlenie tego, czy polecenie zostało pomyślnie zakończone.</span><span class="sxs-lookup"><span data-stu-id="3a331-112">This command enables the Traffic Manager profile named MyProfile and displays whether the command succeeded.</span></span>

## <span data-ttu-id="3a331-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a331-113">PARAMETERS</span></span>

### <span data-ttu-id="3a331-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a331-114">-Name</span></span>
<span data-ttu-id="3a331-115">Określa nazwę profilu usługi Traffic Manager, który ma zostać włączony.</span><span class="sxs-lookup"><span data-stu-id="3a331-115">Specifies the name of the Traffic Manager profile to enable.</span></span>

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

### <span data-ttu-id="3a331-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a331-116">-PassThru</span></span>
<span data-ttu-id="3a331-117">Zwraca $True, jeśli operacja zakończyła się pomyślnie; w przeciwnym razie $False.</span><span class="sxs-lookup"><span data-stu-id="3a331-117">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="3a331-118">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3a331-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a331-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="3a331-119">-Profile</span></span>
<span data-ttu-id="3a331-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a331-120">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3a331-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3a331-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a331-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a331-122">CommonParameters</span></span>
<span data-ttu-id="3a331-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a331-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a331-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a331-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a331-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a331-125">INPUTS</span></span>

## <span data-ttu-id="3a331-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a331-126">OUTPUTS</span></span>

### <span data-ttu-id="3a331-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3a331-127">System.Boolean</span></span>
<span data-ttu-id="3a331-128">To polecenie cmdlet generuje $True lub $False.</span><span class="sxs-lookup"><span data-stu-id="3a331-128">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="3a331-129">Jeśli operacja powiedzie się i określisz parametr *PassThru* , to polecenie cmdlet zwróci wartość $true.</span><span class="sxs-lookup"><span data-stu-id="3a331-129">If the operation succeeds and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="3a331-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a331-130">NOTES</span></span>

## <span data-ttu-id="3a331-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a331-131">RELATED LINKS</span></span>

[<span data-ttu-id="3a331-132">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3a331-132">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="3a331-133">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3a331-133">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="3a331-134">Nowe — AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3a331-134">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="3a331-135">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3a331-135">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="3a331-136">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3a331-136">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


