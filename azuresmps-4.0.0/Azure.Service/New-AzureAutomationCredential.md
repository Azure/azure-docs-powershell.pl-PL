---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E42F05D0-28AD-4772-9F53-BCE6EFC698AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc7d44b87c1e371f0d0c065746dae991cff1cca8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055187"
---
# <span data-ttu-id="33ae1-101">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="33ae1-101">New-AzureAutomationCredential</span></span>

## <span data-ttu-id="33ae1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33ae1-102">SYNOPSIS</span></span>

<span data-ttu-id="33ae1-103">Tworzy poświadczenie w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="33ae1-103">Creates a credential in Automation.</span></span>

## <span data-ttu-id="33ae1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33ae1-104">SYNTAX</span></span>

```
New-AzureAutomationCredential -Name <String> [-Description <String>] -Value <PSCredential>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="33ae1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="33ae1-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="33ae1-106">Polecenie cmdlet **New-AzureAutomationCredential** tworzy poświadczenie jako obiekt **PSCredential** w usłudze Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="33ae1-106">The **New-AzureAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="33ae1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33ae1-107">EXAMPLES</span></span>

### <span data-ttu-id="33ae1-108">Przykład 1. Tworzenie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="33ae1-108">Example 1: Create a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="33ae1-109">Te polecenia tworzą poświadczenia o nazwie moje poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="33ae1-109">These commands create a credential named MyCredential.</span></span>
<span data-ttu-id="33ae1-110">Utworzono najpierw obiekt poświadczenia, który zawiera nazwę użytkownika i hasło.</span><span class="sxs-lookup"><span data-stu-id="33ae1-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="33ae1-111">Jest to następnie używane w ostatnim poleceniu do tworzenia poświadczenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="33ae1-111">This is then used in the last command to create the Automation credential.</span></span>

## <span data-ttu-id="33ae1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33ae1-112">PARAMETERS</span></span>

### <span data-ttu-id="33ae1-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="33ae1-113">-AutomationAccountName</span></span>
<span data-ttu-id="33ae1-114">Określa nazwę konta automatyzacji, w którym będą przechowywane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="33ae1-114">Specifies the name of the Automation account the credential will be stored in.</span></span>

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

### <span data-ttu-id="33ae1-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="33ae1-115">-Description</span></span>
<span data-ttu-id="33ae1-116">Określa opis poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="33ae1-116">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="33ae1-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="33ae1-117">-Name</span></span>
<span data-ttu-id="33ae1-118">Określa nazwę poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="33ae1-118">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="33ae1-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="33ae1-119">-Profile</span></span>
<span data-ttu-id="33ae1-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33ae1-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="33ae1-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="33ae1-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="33ae1-122">-Value</span><span class="sxs-lookup"><span data-stu-id="33ae1-122">-Value</span></span>
<span data-ttu-id="33ae1-123">Określa poświadczenia jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="33ae1-123">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="33ae1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ae1-124">CommonParameters</span></span>
<span data-ttu-id="33ae1-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33ae1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ae1-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33ae1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ae1-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33ae1-127">INPUTS</span></span>

## <span data-ttu-id="33ae1-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33ae1-128">OUTPUTS</span></span>

### <span data-ttu-id="33ae1-129">Microsoft. Azure. Commands. Automation. model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="33ae1-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="33ae1-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33ae1-130">NOTES</span></span>

## <span data-ttu-id="33ae1-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33ae1-131">RELATED LINKS</span></span>

[<span data-ttu-id="33ae1-132">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="33ae1-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="33ae1-133">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="33ae1-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="33ae1-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="33ae1-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


