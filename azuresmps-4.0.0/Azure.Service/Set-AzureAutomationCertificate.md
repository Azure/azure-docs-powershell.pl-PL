---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: AE74024A-A12A-4EC4-AF6C-62F921EA2532
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b19d0bb0c95e9d489fe26c1cd74705318cedcf2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055394"
---
# <span data-ttu-id="894f7-101">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="894f7-101">Set-AzureAutomationCertificate</span></span>

## <span data-ttu-id="894f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="894f7-102">SYNOPSIS</span></span>

<span data-ttu-id="894f7-103">Modyfikuje konfigurację certyfikatu automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="894f7-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="894f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="894f7-104">SYNTAX</span></span>

```
Set-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="894f7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="894f7-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="894f7-106">Polecenie cmdlet **Set-AzureAutomationCertificate** modyfikuje konfigurację certyfikatu w usłudze Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="894f7-106">The **Set-AzureAutomationCertificate** cmdlet modifies the configuration of a certificate in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="894f7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="894f7-107">EXAMPLES</span></span>

### <span data-ttu-id="894f7-108">Przykład 1: aktualizowanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="894f7-108">Example 1: Update a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="894f7-109">Te polecenia aktualizują istniejący certyfikat o nazwie Moje certyfikaty w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="894f7-109">These commands update an existing certificate named MyCertificate in Automation.</span></span>
<span data-ttu-id="894f7-110">Pierwsze polecenie tworzy hasło do pliku certyfikatu używanego w drugim poleceniu aktualizującym certyfikat.</span><span class="sxs-lookup"><span data-stu-id="894f7-110">The first command creates the password for the certificate file that is used in the second command that updates the certificate.</span></span>

## <span data-ttu-id="894f7-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="894f7-111">PARAMETERS</span></span>

### <span data-ttu-id="894f7-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="894f7-112">-AutomationAccountName</span></span>
<span data-ttu-id="894f7-113">Określa nazwę konta automatyzacji z certyfikatem.</span><span class="sxs-lookup"><span data-stu-id="894f7-113">Specifies the name of the Automation account with the certificate.</span></span>

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

### <span data-ttu-id="894f7-114">— Opis</span><span class="sxs-lookup"><span data-stu-id="894f7-114">-Description</span></span>
<span data-ttu-id="894f7-115">Określa opis certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="894f7-115">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="894f7-116">— Możliwy do wyeksportowania</span><span class="sxs-lookup"><span data-stu-id="894f7-116">-Exportable</span></span>
<span data-ttu-id="894f7-117">Wskazuje, że certyfikat można wyeksportować.</span><span class="sxs-lookup"><span data-stu-id="894f7-117">Indicates the certificate can be exported.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="894f7-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="894f7-118">-Name</span></span>
<span data-ttu-id="894f7-119">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="894f7-119">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="894f7-120">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="894f7-120">-Password</span></span>
<span data-ttu-id="894f7-121">Określa hasło do pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="894f7-121">Specifies the password for the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="894f7-122">-Path</span><span class="sxs-lookup"><span data-stu-id="894f7-122">-Path</span></span>
<span data-ttu-id="894f7-123">Określa ścieżkę do pliku skryptu, który ma zostać przekazany.</span><span class="sxs-lookup"><span data-stu-id="894f7-123">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="894f7-124">Plik może mieć nazwę cer lub PFX.</span><span class="sxs-lookup"><span data-stu-id="894f7-124">The file can be .cer or .pfx.</span></span>

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

### <span data-ttu-id="894f7-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="894f7-125">-Profile</span></span>
<span data-ttu-id="894f7-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="894f7-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="894f7-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="894f7-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="894f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="894f7-128">CommonParameters</span></span>
<span data-ttu-id="894f7-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="894f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="894f7-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="894f7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="894f7-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="894f7-131">INPUTS</span></span>

## <span data-ttu-id="894f7-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="894f7-132">OUTPUTS</span></span>

### <span data-ttu-id="894f7-133">Microsoft. Azure. Commands. Automation. model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="894f7-133">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="894f7-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="894f7-134">NOTES</span></span>

## <span data-ttu-id="894f7-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="894f7-135">RELATED LINKS</span></span>

[<span data-ttu-id="894f7-136">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="894f7-136">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="894f7-137">Nowe — AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="894f7-137">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="894f7-138">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="894f7-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)


