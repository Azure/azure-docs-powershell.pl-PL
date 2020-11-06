---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
ms.openlocfilehash: 549bc5bb67eab5287bf463f7e816cc0ff597cf52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541975"
---
# <span data-ttu-id="e4e7d-101">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e4e7d-101">Set-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="e4e7d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4e7d-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e7d-103">Modyfikuje konfigurację certyfikatu automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-103">Modifies the configuration of an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4e7d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4e7d-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4e7d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4e7d-105">DESCRIPTION</span></span>
<span data-ttu-id="e4e7d-106">Polecenie cmdlet **Set-AzureRmAutomationCertificate** modyfikuje konfigurację certyfikatu w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-106">The **Set-AzureRmAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="e4e7d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4e7d-107">EXAMPLES</span></span>

### <span data-ttu-id="e4e7d-108">Przykład 1. Modyfikowanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="e4e7d-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e4e7d-109">Pierwsze polecenie konwertuje hasło zwykłego tekstu na ciąg bezpieczny za pomocą polecenia cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="e4e7d-110">Polecenie zapisuje ten obiekt w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="e4e7d-111">Drugie polecenie modyfikuje certyfikat o nazwie ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="e4e7d-112">W poleceniu użyto hasła przechowywanego w $Password.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="e4e7d-113">Polecenie określa nazwę konta i ścieżkę pliku, który jest wysyłany.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="e4e7d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4e7d-114">PARAMETERS</span></span>

### <span data-ttu-id="e4e7d-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e4e7d-115">-AutomationAccountName</span></span>
<span data-ttu-id="e4e7d-116">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet modyfikuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4e7d-117">-DefaultProfile</span></span>
<span data-ttu-id="e4e7d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e4e7d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e7d-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="e4e7d-119">-Description</span></span>
<span data-ttu-id="e4e7d-120">Określa opis certyfikatu modyfikowanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e7d-121">— Możliwy do wyeksportowania</span><span class="sxs-lookup"><span data-stu-id="e4e7d-121">-Exportable</span></span>
<span data-ttu-id="e4e7d-122">Określa, czy można eksportować certyfikat.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-122">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e7d-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4e7d-123">-Name</span></span>
<span data-ttu-id="e4e7d-124">Określa nazwę certyfikatu modyfikowanego przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e7d-125">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="e4e7d-125">-Password</span></span>
<span data-ttu-id="e4e7d-126">Określa hasło do pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-126">Specifies the password for the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e7d-127">-Path</span><span class="sxs-lookup"><span data-stu-id="e4e7d-127">-Path</span></span>
<span data-ttu-id="e4e7d-128">Określa ścieżkę do pliku skryptu, który ma zostać przekazany.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="e4e7d-129">Plik może być plikiem cer lub PFX.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-129">The file can be a .cer file or a .pfx file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e7d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4e7d-130">-ResourceGroupName</span></span>
<span data-ttu-id="e4e7d-131">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e7d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e7d-132">CommonParameters</span></span>
<span data-ttu-id="e4e7d-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4e7d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e7d-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4e7d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e7d-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4e7d-135">INPUTS</span></span>

### <span data-ttu-id="e4e7d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e4e7d-136">System.String</span></span>

### <span data-ttu-id="e4e7d-137">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e4e7d-137">System.Security.SecureString</span></span>

### <span data-ttu-id="e4e7d-138">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e4e7d-138">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e4e7d-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4e7d-139">OUTPUTS</span></span>

### <span data-ttu-id="e4e7d-140">Microsoft. Azure. Commands. Automation. model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="e4e7d-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="e4e7d-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4e7d-141">NOTES</span></span>

## <span data-ttu-id="e4e7d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4e7d-142">RELATED LINKS</span></span>

[<span data-ttu-id="e4e7d-143">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e4e7d-143">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="e4e7d-144">Nowe — AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e4e7d-144">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="e4e7d-145">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e4e7d-145">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)


