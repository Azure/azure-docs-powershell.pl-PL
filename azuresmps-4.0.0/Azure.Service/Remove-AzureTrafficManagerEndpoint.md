---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 50B83AEC-1B32-4089-9804-D388677C3F7E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7388841c48f2f7c6ba0752748b245cce1f8b5c4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055058"
---
# <span data-ttu-id="fde99-101">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fde99-101">Remove-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="fde99-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fde99-102">SYNOPSIS</span></span>
<span data-ttu-id="fde99-103">Umożliwia usunięcie punktu końcowego z profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="fde99-103">Removes an endpoint from a Traffic Manager profile.</span></span>

## <span data-ttu-id="fde99-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fde99-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerEndpoint -DomainName <String> [-Force]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fde99-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fde99-105">DESCRIPTION</span></span>
<span data-ttu-id="fde99-106">Polecenie cmdlet **Remove-AzureTrafficManagerEndpoint** umożliwia usunięcie punktu końcowego z profilu Microsoft Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="fde99-106">The **Remove-AzureTrafficManagerEndpoint** cmdlet removes an endpoint from a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="fde99-107">Po usunięciu punktu końcowego przekazanie wyniku do polecenia cmdlet **Set-AzureTrafficManagerProfile** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="fde99-107">After you remove an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fde99-108">To polecenie cmdlet łączy się z usługą Azure, aby zapisać zmiany.</span><span class="sxs-lookup"><span data-stu-id="fde99-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="fde99-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fde99-109">EXAMPLES</span></span>

### <span data-ttu-id="fde99-110">Przykład 1: Usuwanie punktu końcowego z profilu</span><span class="sxs-lookup"><span data-stu-id="fde99-110">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Remove-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="fde99-111">W pierwszym poleceniu jest używany polecenie cmdlet **Get-AzureTrafficManagerProfile** w celu uzyskania profilu o nazwie ContosoProfile, a następnie zapisanie go w zmiennej $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="fde99-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="fde99-112">Drugie polecenie usuwa punkt końcowy z nazwą domeny Contoso02App.cloudapp.net z profilu usługi Traffic Manager przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="fde99-112">The second command removes an endpoint that has the domain name Contoso02App.cloudapp.net from the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="fde99-113">Polecenie przekazuje obiekt profilu do polecenia cmdlet **Set-AzureTrafficManagerProfile** , aby połączyć się z usługą Azure w celu zapisania zmian.</span><span class="sxs-lookup"><span data-stu-id="fde99-113">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="fde99-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fde99-114">PARAMETERS</span></span>

### <span data-ttu-id="fde99-115">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="fde99-115">-DomainName</span></span>
<span data-ttu-id="fde99-116">Określa nazwę domeny punktu końcowego, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="fde99-116">Specifies the domain name of the endpoint to remove.</span></span>

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

### <span data-ttu-id="fde99-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fde99-117">-Force</span></span>
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

### <span data-ttu-id="fde99-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="fde99-118">-Profile</span></span>
<span data-ttu-id="fde99-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fde99-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="fde99-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="fde99-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fde99-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fde99-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="fde99-122">Określa obiekt profilu usługi Traffic Manager, z którego ma zostać usunięty punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="fde99-122">Specifies the Traffic Manager profile object from which to remove the endpoint.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fde99-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde99-123">CommonParameters</span></span>
<span data-ttu-id="fde99-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fde99-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde99-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fde99-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde99-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fde99-126">INPUTS</span></span>

## <span data-ttu-id="fde99-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fde99-127">OUTPUTS</span></span>

### <span data-ttu-id="fde99-128">Microsoft. platformy windowsazure. Commands. Utilities.. modele. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="fde99-128">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="fde99-129">To polecenie cmdlet generuje obiekt profilu usługi Traffic Manager, który zawiera informacje na temat zaktualizowanego profilu.</span><span class="sxs-lookup"><span data-stu-id="fde99-129">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="fde99-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fde99-130">NOTES</span></span>

## <span data-ttu-id="fde99-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fde99-131">RELATED LINKS</span></span>

[<span data-ttu-id="fde99-132">Dodaj-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fde99-132">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="fde99-133">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fde99-133">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="fde99-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fde99-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="fde99-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fde99-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


