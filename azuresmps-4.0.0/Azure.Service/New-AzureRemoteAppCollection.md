---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 2021B6BC-7B59-4A88-B1DF-598203F58901
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e225702238f9a90891db819753a68f728a482f9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054962"
---
# <span data-ttu-id="b0515-101">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="b0515-101">New-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="b0515-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0515-102">SYNOPSIS</span></span>
<span data-ttu-id="b0515-103">Tworzy kolekcję funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b0515-103">Creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="b0515-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0515-104">SYNTAX</span></span>

### <span data-ttu-id="b0515-105">AllParameterSets (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b0515-105">AllParameterSets (Default)</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-Description <String>] [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b0515-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="b0515-106">AzureVNet</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-VNetName] <String> [-SubnetName] <String> [-DnsServers <String>] [[-Domain] <String>]
 [[-Credential] <PSCredential>] [-OrganizationalUnit <String>] [-Description <String>]
 [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0515-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b0515-107">DESCRIPTION</span></span>
<span data-ttu-id="b0515-108">Polecenie cmdlet **New-AzureRemoteAppCollection** tworzy kolekcję funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b0515-108">The **New-AzureRemoteAppCollection** cmdlet creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="b0515-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0515-109">EXAMPLES</span></span>

### <span data-ttu-id="b0515-110">Przykład 1. Tworzenie kolekcji</span><span class="sxs-lookup"><span data-stu-id="b0515-110">Example 1: Create a collection</span></span>
```
PS C:\> New-AzureRemoteAppCollection -CollectionName "Contoso" -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
```

<span data-ttu-id="b0515-111">To polecenie tworzy kolekcję funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b0515-111">This command creates an Azure RemoteApp collection.</span></span>

### <span data-ttu-id="b0515-112">Przykład 2: Tworzenie kolekcji przy użyciu poświadczeń</span><span class="sxs-lookup"><span data-stu-id="b0515-112">Example 2: Create a collection using credentials</span></span>
```
PS C:\> $cred = Get-Credential corp.contoso.com\admin
PS C:\> New-AzureRemoteAppCollection -CollectionName "ContosoHybrid" -ImageName "Windows Server 2012 R2" -Plan Standard -VNetName azureVNet -Domain Contoso.com -Credential $cred -Description Hybrid
```

<span data-ttu-id="b0515-113">To polecenie tworzy kolekcję funkcji Azure RemoteApp przy użyciu poświadczenia z polecenia cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="b0515-113">This command creates an Azure RemoteApp collection using a credential from the **Get-Credential** cmdlet.</span></span>

## <span data-ttu-id="b0515-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0515-114">PARAMETERS</span></span>

### <span data-ttu-id="b0515-115">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="b0515-115">-CollectionName</span></span>
<span data-ttu-id="b0515-116">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b0515-116">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="b0515-117">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="b0515-117">-Credential</span></span>
<span data-ttu-id="b0515-118">Określa poświadczenia konta usługi, które ma uprawnienie do przyłączenia się do serwerów usługi Azure RemoteApp w domenie.</span><span class="sxs-lookup"><span data-stu-id="b0515-118">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="b0515-119">Aby uzyskać obiekt **PSCredential** , użyj polecenia cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="b0515-119">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0515-120">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="b0515-120">-CustomRdpProperty</span></span>
<span data-ttu-id="b0515-121">Określa niestandardowe właściwości usługi Remote Desktop Protocal (RDP), których można użyć w celu skonfigurowania przekierowywania dysków i innych ustawień.</span><span class="sxs-lookup"><span data-stu-id="b0515-121">Specifies custom Remote Desktop Protocal (RDP) properties which can be used to configure drive redirection and other settings.</span></span>
<span data-ttu-id="b0515-122">Zobacz [Ustawienia protokołu RDP dla usług pulpitu zdalnego w systemie Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) , `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` Aby uzyskać szczegółowe informacje.  </span><span class="sxs-lookup"><span data-stu-id="b0515-122">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

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

### <span data-ttu-id="b0515-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="b0515-123">-Description</span></span>
<span data-ttu-id="b0515-124">Określa Krótki opis obiektu.</span><span class="sxs-lookup"><span data-stu-id="b0515-124">Specifies a short description for the object.</span></span>

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

### <span data-ttu-id="b0515-125">-DnsServers</span><span class="sxs-lookup"><span data-stu-id="b0515-125">-DnsServers</span></span>
<span data-ttu-id="b0515-126">Określa listę adresów IPv4 serwerów DNS rozdzielonych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="b0515-126">Specifies a comma-separated list of IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0515-127">-Domain</span><span class="sxs-lookup"><span data-stu-id="b0515-127">-Domain</span></span>
<span data-ttu-id="b0515-128">Określa nazwę domeny usług domenowych Active Directory, do której ma zostać przyłączony serwer hosta sesji usług pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="b0515-128">Specifies the name of the Active Directory Domain Services domain to which to join the RD Session Host servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0515-129">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b0515-129">-ImageName</span></span>
<span data-ttu-id="b0515-130">Określa nazwę obrazu szablonu usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b0515-130">Specifies the name of the Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0515-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b0515-131">-Location</span></span>
<span data-ttu-id="b0515-132">Określa obszar Azure kolekcji.</span><span class="sxs-lookup"><span data-stu-id="b0515-132">Specifies the Azure region of the collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0515-133">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="b0515-133">-OrganizationalUnit</span></span>
<span data-ttu-id="b0515-134">Określa nazwę jednostki organizacyjnej, do której ma zostać przyłączone serwery hosta sesji usług pulpitu zdalnego, na przykład OU = MyOu, DC = moja domena, DC = ParentDomain, DC = com.</span><span class="sxs-lookup"><span data-stu-id="b0515-134">Specifies the name of the organizational unit (OU) to which to join the RD Session Host servers, for example, OU=MyOu,DC=MyDomain,DC=ParentDomain,DC=com.</span></span>
<span data-ttu-id="b0515-135">Atrybuty, takie jak OU i DC, muszą być pisane wielkimi literami.</span><span class="sxs-lookup"><span data-stu-id="b0515-135">Attributes such as OU and DC must be in uppercase.</span></span>
<span data-ttu-id="b0515-136">Nie można zmienić jednostki organizacyjnej po utworzeniu kolekcji.</span><span class="sxs-lookup"><span data-stu-id="b0515-136">The OU cannot be changed after the collection has been created.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0515-137">-Plan</span><span class="sxs-lookup"><span data-stu-id="b0515-137">-Plan</span></span>
<span data-ttu-id="b0515-138">Określa plan kolekcji funkcji RemoteApp usługi Azure, który może definiować limity użycia.</span><span class="sxs-lookup"><span data-stu-id="b0515-138">Specifies the plan for the Azure RemoteApp collection, which may define the usage limits.</span></span>
<span data-ttu-id="b0515-139">Użyj **Get-AzureRemoteAppPlan** , aby wyświetlić dostępne plany.</span><span class="sxs-lookup"><span data-stu-id="b0515-139">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0515-140">-Profile</span><span class="sxs-lookup"><span data-stu-id="b0515-140">-Profile</span></span>
<span data-ttu-id="b0515-141">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0515-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b0515-142">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b0515-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b0515-143">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b0515-143">-ResourceType</span></span>
<span data-ttu-id="b0515-144">Określa typ zasobu kolekcji.</span><span class="sxs-lookup"><span data-stu-id="b0515-144">Specifies the resource type of the collection.</span></span>
<span data-ttu-id="b0515-145">Dopuszczalne wartości tego parametru to: aplikacja lub pulpit.</span><span class="sxs-lookup"><span data-stu-id="b0515-145">The acceptable values for this parameter are: App or Desktop.</span></span>

```yaml
Type: CollectionMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0515-146">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="b0515-146">-SubnetName</span></span>
<span data-ttu-id="b0515-147">Określa nazwę podsieci w sieci wirtualnej używanej do tworzenia kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b0515-147">Specifies the name of the subnet in the virtual network to use to create the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0515-148">-VNetName</span><span class="sxs-lookup"><span data-stu-id="b0515-148">-VNetName</span></span>
<span data-ttu-id="b0515-149">Określa nazwę sieci wirtualnej usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b0515-149">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0515-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0515-150">CommonParameters</span></span>
<span data-ttu-id="b0515-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0515-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0515-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0515-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0515-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0515-153">INPUTS</span></span>

## <span data-ttu-id="b0515-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0515-154">OUTPUTS</span></span>

## <span data-ttu-id="b0515-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0515-155">NOTES</span></span>

## <span data-ttu-id="b0515-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0515-156">RELATED LINKS</span></span>

[<span data-ttu-id="b0515-157">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="b0515-157">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="b0515-158">Get-AzureRemoteAppPlan</span><span class="sxs-lookup"><span data-stu-id="b0515-158">Get-AzureRemoteAppPlan</span></span>](./Get-AzureRemoteAppPlan.md)

[<span data-ttu-id="b0515-159">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="b0515-159">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="b0515-160">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="b0515-160">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="b0515-161">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="b0515-161">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


