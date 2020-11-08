---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054502"
---
# <span data-ttu-id="53cb6-101">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="53cb6-101">Get-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="53cb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="53cb6-103">Pobiera szczegóły profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="53cb6-103">Gets the details of a Traffic Manager profile.</span></span>

## <span data-ttu-id="53cb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53cb6-104">SYNTAX</span></span>

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="53cb6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="53cb6-105">DESCRIPTION</span></span>
<span data-ttu-id="53cb6-106">Polecenie cmdlet **Get-AzureTrafficManagerProfile** pobiera szczegóły profilu Microsoft Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="53cb6-106">The **Get-AzureTrafficManagerProfile** cmdlet gets the details of a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="53cb6-107">Jeśli parametr *name* nie jest określony, polecenie cmdlet wyświetla listę profilów usługi Traffic managera w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="53cb6-107">If you do not specify the *Name* parameter, the cmdlet lists the Traffic Manager profiles in the current subscription.</span></span>

## <span data-ttu-id="53cb6-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53cb6-108">EXAMPLES</span></span>

### <span data-ttu-id="53cb6-109">Przykład 1: uzyskiwanie listy profilów usługi Traffic managera w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="53cb6-109">Example 1: Get the list of Traffic Manager profiles in a subscription</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile
```

<span data-ttu-id="53cb6-110">To polecenie pobiera listę profilów usługi Traffic managera w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="53cb6-110">This command gets the list of Traffic Manager profiles in your subscription.</span></span>

### <span data-ttu-id="53cb6-111">Przykład 2: uzyskiwanie profilu w usłudze Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="53cb6-111">Example 2: Get a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="53cb6-112">To polecenie pobiera profil usługi Traffic Manager o nazwie Moja profil.</span><span class="sxs-lookup"><span data-stu-id="53cb6-112">This command gets the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="53cb6-113">Przykład 3: Dodawanie punktu końcowego do profilu usługi Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="53cb6-113">Example 3: Add an endpoint to a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="53cb6-114">To polecenie dodaje punkt końcowy do profilu usługi Traffic Manager, a następnie zapisuje profil.</span><span class="sxs-lookup"><span data-stu-id="53cb6-114">This command adds an endpoint to a Traffic Manager profile, and then saves the profile.</span></span>

## <span data-ttu-id="53cb6-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53cb6-115">PARAMETERS</span></span>

### <span data-ttu-id="53cb6-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="53cb6-116">-Name</span></span>
<span data-ttu-id="53cb6-117">Określa nazwę profilu usługi Traffic Manager, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="53cb6-117">Specifies the name of the Traffic Manager profile to get.</span></span>

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

### <span data-ttu-id="53cb6-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="53cb6-118">-Profile</span></span>
<span data-ttu-id="53cb6-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53cb6-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="53cb6-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="53cb6-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="53cb6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53cb6-121">CommonParameters</span></span>
<span data-ttu-id="53cb6-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53cb6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53cb6-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53cb6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53cb6-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53cb6-124">INPUTS</span></span>

## <span data-ttu-id="53cb6-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53cb6-125">OUTPUTS</span></span>

### <span data-ttu-id="53cb6-126">Microsoft. platformy windowsazure. Commands. Utilities.. modele. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="53cb6-126">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="53cb6-127">To polecenie cmdlet generuje obiekt lub obiekty profilu Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="53cb6-127">This cmdlet generates a Traffic Manager profile object or objects.</span></span>

## <span data-ttu-id="53cb6-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53cb6-128">NOTES</span></span>

## <span data-ttu-id="53cb6-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53cb6-129">RELATED LINKS</span></span>

[<span data-ttu-id="53cb6-130">Dodaj-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="53cb6-130">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="53cb6-131">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="53cb6-131">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="53cb6-132">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="53cb6-132">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="53cb6-133">Nowe — AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="53cb6-133">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="53cb6-134">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="53cb6-134">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="53cb6-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="53cb6-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


