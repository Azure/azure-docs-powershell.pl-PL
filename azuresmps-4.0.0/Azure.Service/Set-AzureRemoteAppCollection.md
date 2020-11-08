---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 14B4050D-3597-4760-A152-82617B88078D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 291ea94bbdfff1da8d658074ebfb72df8943f0e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055019"
---
# <span data-ttu-id="2227b-101">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="2227b-101">Set-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="2227b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2227b-102">SYNOPSIS</span></span>
<span data-ttu-id="2227b-103">Ustawia właściwości kolekcji funkcji RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="2227b-103">Sets the properties of a RemoteApp collection.</span></span>

## <span data-ttu-id="2227b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2227b-104">SYNTAX</span></span>

### <span data-ttu-id="2227b-105">DescriptionOnly (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2227b-105">DescriptionOnly (Default)</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Description <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="2227b-106">PlanOnly</span><span class="sxs-lookup"><span data-stu-id="2227b-106">PlanOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Plan <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="2227b-107">DomainJoined</span><span class="sxs-lookup"><span data-stu-id="2227b-107">DomainJoined</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="2227b-108">RdpPropertyOnly</span><span class="sxs-lookup"><span data-stu-id="2227b-108">RdpPropertyOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -CustomRdpProperty <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="2227b-109">AclLevelOnly</span><span class="sxs-lookup"><span data-stu-id="2227b-109">AclLevelOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -AclLevel <CollectionAclLevel>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2227b-110">Opis</span><span class="sxs-lookup"><span data-stu-id="2227b-110">DESCRIPTION</span></span>
<span data-ttu-id="2227b-111">Polecenie cmdlet **Set-AzureRemoteAppCollection** ustawia właściwości kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="2227b-111">The **Set-AzureRemoteAppCollection** cmdlet sets the properties of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="2227b-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2227b-112">EXAMPLES</span></span>

## <span data-ttu-id="2227b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2227b-113">PARAMETERS</span></span>

### <span data-ttu-id="2227b-114">-AclLevel</span><span class="sxs-lookup"><span data-stu-id="2227b-114">-AclLevel</span></span>
<span data-ttu-id="2227b-115">Określa poziom listy kontroli dostępu (ACL) dla kolekcji.</span><span class="sxs-lookup"><span data-stu-id="2227b-115">Specifies the access control list (ACL) level for the collection.</span></span>
<span data-ttu-id="2227b-116">Dopuszczalne wartości tego parametru to: kolekcja i aplikacja.</span><span class="sxs-lookup"><span data-stu-id="2227b-116">The acceptable values for this parameter are: Collection and Application.</span></span>

```yaml
Type: CollectionAclLevel
Parameter Sets: AclLevelOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2227b-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="2227b-117">-CollectionName</span></span>
<span data-ttu-id="2227b-118">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="2227b-118">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2227b-119">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="2227b-119">-Credential</span></span>
<span data-ttu-id="2227b-120">Określa poświadczenia konta usługi, które ma uprawnienie do przyłączenia się do serwerów usługi Azure RemoteApp w domenie.</span><span class="sxs-lookup"><span data-stu-id="2227b-120">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="2227b-121">Aby uzyskać obiekt **PSCredential** , użyj polecenia cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="2227b-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: DomainJoined
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2227b-122">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="2227b-122">-CustomRdpProperty</span></span>
<span data-ttu-id="2227b-123">Określa niestandardowe właściwości protokołu RDP (Remote Desktop Protocol), których można użyć w celu skonfigurowania przekierowywania dysków i innych ustawień.</span><span class="sxs-lookup"><span data-stu-id="2227b-123">Specifies custom Remote Desktop Protocol (RDP) properties which can be used to configure drive redirection and other settings.</span></span> <span data-ttu-id="2227b-124">Zobacz [Ustawienia protokołu RDP dla usług pulpitu zdalnego w systemie Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) , `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` Aby uzyskać szczegółowe informacje.  </span><span class="sxs-lookup"><span data-stu-id="2227b-124">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

```yaml
Type: String
Parameter Sets: RdpPropertyOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2227b-125">— Opis</span><span class="sxs-lookup"><span data-stu-id="2227b-125">-Description</span></span>
<span data-ttu-id="2227b-126">Określa Krótki opis kolekcji.</span><span class="sxs-lookup"><span data-stu-id="2227b-126">Specifies a short description for the collection.</span></span>

```yaml
Type: String
Parameter Sets: DescriptionOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2227b-127">-Plan</span><span class="sxs-lookup"><span data-stu-id="2227b-127">-Plan</span></span>
<span data-ttu-id="2227b-128">Określa plan kolekcji usługi Azure RemoteApp definiujący limity użycia.</span><span class="sxs-lookup"><span data-stu-id="2227b-128">Specifies the plan for the Azure RemoteApp collection, which defines the usage limits.</span></span>
<span data-ttu-id="2227b-129">Użyj **Get-AzureRemoteAppPlan** , aby wyświetlić dostępne plany.</span><span class="sxs-lookup"><span data-stu-id="2227b-129">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: PlanOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2227b-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="2227b-130">-Profile</span></span>
<span data-ttu-id="2227b-131">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2227b-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2227b-132">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2227b-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2227b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2227b-133">CommonParameters</span></span>
<span data-ttu-id="2227b-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2227b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2227b-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2227b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2227b-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2227b-136">INPUTS</span></span>

## <span data-ttu-id="2227b-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2227b-137">OUTPUTS</span></span>

## <span data-ttu-id="2227b-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2227b-138">NOTES</span></span>

## <span data-ttu-id="2227b-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2227b-139">RELATED LINKS</span></span>

[<span data-ttu-id="2227b-140">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="2227b-140">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="2227b-141">Nowe — AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="2227b-141">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="2227b-142">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="2227b-142">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


