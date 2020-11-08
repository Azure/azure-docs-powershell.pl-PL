---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055443"
---
# <span data-ttu-id="2f5f9-101">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="2f5f9-101">Remove-AzureEnvironment</span></span>

## <span data-ttu-id="2f5f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f5f9-102">SYNOPSIS</span></span>
<span data-ttu-id="2f5f9-103">Usuwa środowisko Azure z programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-103">Deletes an Azure environment from Windows PowerShell.</span></span>

## <span data-ttu-id="2f5f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f5f9-104">SYNTAX</span></span>

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2f5f9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2f5f9-105">DESCRIPTION</span></span>
<span data-ttu-id="2f5f9-106">Polecenie cmdlet **Remove-AzureEnvironment** usuwa środowisko Azure z profilu mobilnego, więc program Windows PowerShell nie może go znaleźć.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-106">The **Remove-AzureEnvironment** cmdlet deletes an Azure environment from your roaming profile so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="2f5f9-107">To polecenie cmdlet nie powoduje usunięcia środowiska z platformy Microsoft Azure ani w jakikolwiek sposób zmieniania rzeczywistego środowiska.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-107">This cmdlet does not delete the environment from Microsoft Azure, or change the actual environment in any way.</span></span>

<span data-ttu-id="2f5f9-108">Środowisko platformy Azure niezależne wdrożenie platformy Microsoft Azure, takiej jak AzureCloud dla usługi Azure i AzureChinaCloud dla platformy Azure obsługiwanej przez firmę 21Vianet w Chinach.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-108">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="2f5f9-109">Lokalne środowiska platformy Azure można też tworzyć, korzystając z pakietu Azure i poleceń cmdlet WAPack.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-109">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="2f5f9-110">Aby uzyskać więcej informacji, zobacz [pakiet Azure](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2f5f9-110">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

## <span data-ttu-id="2f5f9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f5f9-111">EXAMPLES</span></span>

### <span data-ttu-id="2f5f9-112">Przykład 1: usuwanie środowiska</span><span class="sxs-lookup"><span data-stu-id="2f5f9-112">Example 1: Delete an environment</span></span>
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

<span data-ttu-id="2f5f9-113">To polecenie usuwa środowisko ContosoEnv z programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-113">This command deletes the ContosoEnv environment from Windows PowerShell.</span></span>

### <span data-ttu-id="2f5f9-114">Przykład 2: usuwanie wielu środowisk</span><span class="sxs-lookup"><span data-stu-id="2f5f9-114">Example 2: Delete multiple environments</span></span>
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

<span data-ttu-id="2f5f9-115">To polecenie usuwa środowiska, których nazwy zaczynają się od ciągu "contoso" w programie Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-115">This command deletes environments whose names begin with "Contoso" from Windows PowerShell.</span></span>

## <span data-ttu-id="2f5f9-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f5f9-116">PARAMETERS</span></span>

### <span data-ttu-id="2f5f9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2f5f9-117">-Force</span></span>
<span data-ttu-id="2f5f9-118">Pomija monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-118">Suppresses the confirmation prompt.</span></span>

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

### <span data-ttu-id="2f5f9-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2f5f9-119">-Name</span></span>
<span data-ttu-id="2f5f9-120">Określa nazwę środowiska, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-120">Specifies the name of the environment to remove.</span></span>
<span data-ttu-id="2f5f9-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-121">This parameter is required.</span></span>
<span data-ttu-id="2f5f9-122">W tej wartości parametru jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-122">This parameter value is case-sensitive.</span></span>
<span data-ttu-id="2f5f9-123">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-123">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="2f5f9-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="2f5f9-124">-Profile</span></span>
<span data-ttu-id="2f5f9-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2f5f9-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2f5f9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f5f9-127">CommonParameters</span></span>
<span data-ttu-id="2f5f9-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f5f9-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f5f9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f5f9-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f5f9-130">INPUTS</span></span>

### <span data-ttu-id="2f5f9-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2f5f9-131">None</span></span>
<span data-ttu-id="2f5f9-132">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-132">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="2f5f9-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f5f9-133">OUTPUTS</span></span>

### <span data-ttu-id="2f5f9-134">Brak lub system. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f5f9-134">None or System.Boolean</span></span>
<span data-ttu-id="2f5f9-135">W przypadku użycia parametru *PassThru* to polecenie cmdlet zwraca wartość logiczną.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-135">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="2f5f9-136">W przeciwnym razie nie zwróci żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2f5f9-136">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="2f5f9-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f5f9-137">NOTES</span></span>

## <span data-ttu-id="2f5f9-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f5f9-138">RELATED LINKS</span></span>

[<span data-ttu-id="2f5f9-139">Dodaj-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="2f5f9-139">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="2f5f9-140">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="2f5f9-140">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="2f5f9-141">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="2f5f9-141">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


